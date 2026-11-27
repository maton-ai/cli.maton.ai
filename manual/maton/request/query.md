---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton request query

```
maton request query [<sql>] [flags]
```

Run one read-only SQL SELECT over your account's requests, for questions
`list` and `maton metric query` cannot answer. The dialect is ClickHouse.

The only table is `requests`, which holds your account's requests from the
last 30 days. Its columns are:

  request_id, account_id, source, connection_id, app, client_ip,
  user_agent, duration_ms, start_time, end_time, request_method,
  request_host, request_path, request_query_params, request_headers,
  request_body_size, response_status_code, response_headers,
  response_body_size, upstream_duration_ms, upstream_request_method,
  upstream_request_host, upstream_request_path,
  upstream_request_query_params, upstream_request_headers,
  upstream_response_status_code, upstream_response_headers

Bodies are not queryable; fetch them with `maton request get`.

Pass the SQL as an argument, or read it with `--file`. To keep values out
of the SQL text, write a `{name:Type}` placeholder and supply it with
`--param name=value`.

A query returns at most 1000 rows and may run for 10 seconds. Filter on
start_time to keep it fast.


### Options


<dl class="flags">
	<dt><code>-f</code>, 
		<code>--file &lt;file&gt;</code></dt>
	<dd>Read the SQL from file (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output the rows as JSON</dd>

	<dt>
		<code>--param &lt;name=value&gt;</code></dt>
	<dd>Set a query parameter in name=value format</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>
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
# Requests per app over the last day
$ maton request query "SELECT app, count() AS requests FROM requests WHERE start_time > now() - INTERVAL 1 DAY GROUP BY app ORDER BY requests DESC"

# The slowest requests at or above a status code
$ maton request query "SELECT request_id, duration_ms FROM requests WHERE response_status_code >= {min:UInt16} ORDER BY duration_ms DESC LIMIT 10" --param min=500

# A query kept in a file, as JSON
$ maton request query --file slow.sql --json

# From standard input
$ echo "SELECT count() FROM requests" | maton request query --file -
{% endraw %}{% endhighlight %}

### See also

* [maton request](/manual/maton/request)
