---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton request list

```
maton request list [flags]
```

List the most recent requests in your account, newest first.

Without `--since` the window is the last 24 hours. `--since` and `--until`
take an RFC3339 timestamp or a duration such as `10m` or `7d`,
meaning that long ago. Requests are kept for 30 days.

`--status` takes a status code (`404`), a class (`5xx`), or a comparison
(`">=400"`). See `maton request --help` for the `--search` query syntax.

Pass a request's ID to `maton request get` for its headers and bodies.


### Options


<dl class="flags">
	<dt>
		<code>--app &lt;string&gt;</code></dt>
	<dd>Filter by app, such as slack</dd>

	<dt>
		<code>--connection &lt;id&gt;</code></dt>
	<dd>Filter by connection id</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 30)</code></dt>
	<dd>Maximum number of requests to fetch (0 = no limit)</dd>

	<dt>
		<code>--method &lt;string&gt;</code></dt>
	<dd>Filter by HTTP method, such as POST</dd>

	<dt><code>-S</code>, 
		<code>--search &lt;string&gt;</code></dt>
	<dd>Filter with a search query</dd>

	<dt>
		<code>--since &lt;string&gt;</code></dt>
	<dd>Start of the window: RFC3339 or a duration like 10m or 7d</dd>

	<dt>
		<code>--source &lt;string&gt;</code></dt>
	<dd>Filter by source, such as gateway</dd>

	<dt>
		<code>--status &lt;code&gt;</code></dt>
	<dd>Filter by response status: a code, a class like 5xx, or a comparison like &#34;&gt;=400&#34;</dd>

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

 maton requests ls, maton request ls

### JSON Fields

`account_id`, `app`, `client_ip`, `connection_id`, `duration_ms`, `end_time`, `request_host`, `request_id`, `request_method`, `request_path`, `response_status_code`, `source`, `start_time`, `user_agent`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# The latest 30 requests from the last 24 hours
$ maton request list

# Failed Slack requests from the last hour
$ maton request list --app slack --status ">=400" --since 1h

# Server errors on one connection
$ maton request list --connection 21fd90f9-5935-43cd-b6c8-bde9d915ca80 --status 5xx

# Slow requests under a path, as JSON
$ maton request list -S "duration_ms:>2000 AND request_path:/slack/api/*" --json request_id,duration_ms
{% endraw %}{% endhighlight %}

### See also

* [maton request](/manual/maton/request)
