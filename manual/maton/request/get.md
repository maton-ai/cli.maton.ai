---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton request get

```
maton request get <request-id> [flags]
```

Show everything recorded for one request: where it came from, what was
sent and returned, including headers and bodies.

A small body is printed inline. A large one is stored separately and
shown as a download link that expires after 15 minutes; run the command
again for a fresh link.

The request ID is the `ID` column of `maton request list`, and the
`request_id` of a log.


### Options


<dl class="flags">
	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

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


### ALIASES

 maton requests view, maton request view

### JSON Fields

`account_id`, `app`, `client_ip`, `connection_id`, `duration_ms`, `end_time`, `request_body`, `request_body_size`, `request_body_url`, `request_headers`, `request_host`, `request_id`, `request_method`, `request_path`, `request_query_params`, `response_body`, `response_body_size`, `response_body_url`, `response_headers`, `response_status_code`, `source`, `start_time`, `upstream_duration_ms`, `upstream_request_headers`, `upstream_request_host`, `upstream_request_method`, `upstream_request_path`, `upstream_request_query_params`, `upstream_response_headers`, `upstream_response_status_code`, `user_agent`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton request get 0198c1a2-7b3c-7d4e-8f5a-6b7c8d9e0f1a

# Just the response body
$ maton request get 0198c1a2-7b3c-7d4e-8f5a-6b7c8d9e0f1a --json response_body --jq .response_body

# Download a large response body
$ curl -o body "$(maton request get 0198c1a2-7b3c-7d4e-8f5a-6b7c8d9e0f1a --json response_body_url --jq .response_body_url)"
{% endraw %}{% endhighlight %}

### See also

* [maton request](/manual/maton/request)
