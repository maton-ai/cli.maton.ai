---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton metric

Aggregate the requests and logs Maton records for your account: counts,
latencies, and payload sizes, as totals or as a time series, optionally
split by a facet such as app or status code.

Data is kept for 30 days. There are two data sources:

requests (default)
  Metrics: duration_ms, upstream_duration_ms, overhead_ms,
    request_body_size, response_body_size
  Facets: source, app, connection_id, request_method, request_host,
    response_status_code, upstream_request_host,
    upstream_response_status_code, user_agent

logs
  Metrics: none, so only count and cardinality apply
  Facets: level, source

Aggregations are count, sum, avg, min, max, stddev, median, and `pc<n>`
for any percentile, such as pc95 or pc99.9. `cardinality` counts the distinct
values of a facet, named with `--metric`.

`--search` narrows the rows that are aggregated. `field:value` terms match the
facets above (plus request_path and duration_ms for requests, and
request_id for logs); bare words match the log message. Terms combine
with AND, OR, NOT, and parentheses, and `*` and `?` are wildcards.


### Available commands

* [maton metric query](/manual/maton/metric/query)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton metrics

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton metric query
$ maton metric query --aggregation pc95 --metric duration_ms --since 24h
$ maton metric query --group-by app --interval 5m
$ maton metric query --input error-rate.json
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
