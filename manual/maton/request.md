---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton request

Inspect the API requests Maton records for your account. `list` returns
recent requests, `get` shows one in full, with its headers and bodies, and
`query` runs a SQL SELECT over all of them.

Requests are kept for 30 days.

`--search` on `list` takes a query made of `field:value` terms. The fields are
source, app, connection_id, request_method, request_host, request_path,
response_status_code, duration_ms, user_agent, upstream_request_host, and
upstream_response_status_code. The two status codes and duration_ms also
take comparisons and ranges, such as `duration_ms:>1000` or
`response_status_code:[400 TO 499]`. Terms combine with AND, OR, NOT, and
parentheses, and `*` and `?` are wildcards. There is no free-text search.


### Available commands

* [maton request get](/manual/maton/request/get)
* [maton request list](/manual/maton/request/list)
* [maton request query](/manual/maton/request/query)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton requests

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton request list
$ maton request list --app slack --status ">=400" --since 1h
$ maton request get 0198c1a2-7b3c-7d4e-8f5a-6b7c8d9e0f1a
$ maton request query "SELECT app, count() AS requests FROM requests GROUP BY app"
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
