---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton metric query

```
maton metric query [flags]
```

Compute one aggregation over your account's requests or logs. Without
flags it counts the requests of the last hour.

`--metric` names what to aggregate and `--aggregation` how. Without
`--aggregation` the metric's default applies: avg for durations, sum for
sizes. `--group-by` splits the result by a facet and can be repeated up to
three times; `--limit` keeps the top groups of each facet, 10 by default.

Without `--interval` the result is one total per group. With it, the
result is a time series with one row per bucket and group. The interval
is a whole number of minutes, and long windows raise it to keep the
number of buckets bounded. The table leaves out the rows of a bucket
where a group has no value; `--json` keeps them, with null values.

`--since` and `--until` take an RFC3339 timestamp or a duration such as
`10m` or `7d`, meaning that long ago. The default window is the last hour.

`--input` sends a JSON request body from a file instead, for several
queries at once and formulas over them, such as an error rate. The time
flags still apply and override the body's from, to, and interval.

`--json` prints the same rows as a list of objects keyed by column name:
the facets, then one key per query or formula, after `time` for a time
series. A query built from flags is named after what it computes, such
as `count` or `pc95_duration_ms`, or `value` when that name would match a
facet it is grouped by. Numbers keep full precision and carry no unit, a
missing value is null, and an empty facet value is an empty string.

See `maton metric --help` for the metrics, facets, and search syntax.


### Options


<dl class="flags">
	<dt><code>-a</code>, 
		<code>--aggregation &lt;string&gt;</code></dt>
	<dd>How to aggregate, such as count, avg, or pc95</dd>

	<dt>
		<code>--data-source &lt;string&gt;</code></dt>
	<dd>Data to aggregate: requests or logs (default &#34;requests&#34;)</dd>

	<dt><code>-g</code>, 
		<code>--group-by &lt;stringArray&gt;</code></dt>
	<dd>Split the result by a facet, such as app</dd>

	<dt>
		<code>--input &lt;file&gt;</code></dt>
	<dd>Read the JSON request body from file (use &#34;-&#34; to read from standard input)</dd>

	<dt>
		<code>--interval &lt;duration&gt;</code></dt>
	<dd>Return a time series with buckets of this size, such as 5m or 1d</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output the rows as JSON</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Maximum number of groups per facet (default 10)</dd>

	<dt><code>-m</code>, 
		<code>--metric &lt;string&gt;</code></dt>
	<dd>What to aggregate, such as duration_ms</dd>

	<dt>
		<code>--order &lt;string&gt;</code></dt>
	<dd>Keep the smallest or the largest groups: {asc|desc}</dd>

	<dt><code>-S</code>, 
		<code>--search &lt;string&gt;</code></dt>
	<dd>Aggregate only what matches a search query</dd>

	<dt>
		<code>--since &lt;string&gt;</code></dt>
	<dd>Start of the window: RFC3339 or a duration like 10m or 7d</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--until &lt;string&gt;</code></dt>
	<dd>End of the window: RFC3339 or a duration like 10m or 7d</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# Requests in the last hour
$ maton metric query

# 95th percentile latency over the last day
$ maton metric query --aggregation pc95 --metric duration_ms --since 24h

# Top 5 apps by request count
$ maton metric query --group-by app --limit 5

# Average Slack latency in 5 minute buckets
$ maton metric query --metric duration_ms --search app:slack --interval 5m

# Error logs by source over the last week
$ maton metric query --data-source logs --search level:error --group-by source --since 7d

# The busiest app, as JSON
$ maton metric query --group-by app --json --jq '.[0].app'

# Error rate per app, from a request body with two queries and a formula
$ maton metric query --since 24h --input - <<'EOF'
{
  "queries": [
    {"name": "errors", "compute": {"aggregation": "count"},
     "search": {"query": "response_status_code:>=500"}, "group_by": [{"facet": "app"}]},
    {"name": "total", "compute": {"aggregation": "count"}, "group_by": [{"facet": "app"}]}
  ],
  "formulas": [{"name": "error_rate", "formula": "errors / total * 100"}]
}
EOF
{% endraw %}{% endhighlight %}

### See also

* [maton metric](/manual/maton/metric)
