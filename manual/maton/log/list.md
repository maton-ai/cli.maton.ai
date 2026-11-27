---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton log list

```
maton log list [flags]
```

List the most recent logs in your account, newest first.

Without `--since` the window is the last 24 hours. `--since` and `--until`
take an RFC3339 timestamp or a duration such as `10m` or `7d`,
meaning that long ago. Logs are kept for 30 days. To follow new logs
instead of taking a snapshot, use `maton log tail`.

See `maton log --help` for the `--search` query syntax.


### Options


<dl class="flags">
	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt>
		<code>--level &lt;string&gt;</code></dt>
	<dd>Filter by level: {info|warning|error}</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 100)</code></dt>
	<dd>Maximum number of logs to fetch (0 = no limit)</dd>

	<dt>
		<code>--request-id &lt;string&gt;</code></dt>
	<dd>Filter by the request that wrote the log</dd>

	<dt><code>-S</code>, 
		<code>--search &lt;string&gt;</code></dt>
	<dd>Filter with a search query</dd>

	<dt>
		<code>--since &lt;string&gt;</code></dt>
	<dd>Start of the window: RFC3339 or a duration like 10m or 7d</dd>

	<dt>
		<code>--source &lt;string&gt;</code></dt>
	<dd>Filter by source, such as gateway or function</dd>

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


### ALIASES

 maton logs ls, maton log ls

### JSON Fields

`level`, `log_id`, `message`, `request_id`, `source`, `timestamp`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# The latest 100 logs from the last 24 hours
$ maton log list

# Errors from the last hour
$ maton log list --level error --since 1h

# Everything one request wrote
$ maton log list --request-id 0198c1a2-7b3c-7d4e-8f5a-6b7c8d9e0f1a

# Gateway logs mentioning a timeout, as JSON
$ maton log list --source gateway --search timeout --json timestamp,level,message
{% endraw %}{% endhighlight %}

### See also

* [maton log](/manual/maton/log)
