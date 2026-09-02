---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function run get

```
maton function run get <run-id> --function <function-id> [flags]
```

Show the request a run received and the response it produced.

What is shown is the request as recorded, which is not quite the event the
handler was given. The method, path, and query string match, and the body is
a string here as it is there. The headers do not: the service redacts
authorization, cookie, x-api-key and friends before recording, and drops
cookies outright, while the handler is handed the real ones. Query params,
headers, and the query string are truncated to a size budget too. So what you
see is what was recorded, not what arrived — and not what ran.

See `maton function --help` for the event's own shape.

An invocation answers with the run's ID in `X-Function-Run-Id`, so
`maton api <url> -i` names the run to pass here.


### Options


<dl class="flags">
	<dt><code>-f</code>, 
		<code>--function &lt;string&gt;</code></dt>
	<dd>Function ID this resource belongs to (required)</dd>

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

 maton function runs view,  maton functions run view,  maton functions runs view, maton function run view

### JSON Fields

`created_at`, `ended_at`, `function_id`, `request`, `response`, `run_id`, `started_at`, `version`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton function run get run_abc123 --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function run get run_abc123 -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --json response
{% endraw %}{% endhighlight %}

### See also

* [maton function run](/manual/maton/function/run)
