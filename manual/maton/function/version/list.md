---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function version list

```
maton function version list --function <function-id> [flags]
```

List a function's code versions, newest first.

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

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Maximum number of versions to fetch (0 = no limit)</dd>

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

 maton function versions ls,  maton functions version ls,  maton functions versions ls, maton function version ls

### JSON Fields

`code_sha256`, `code_size`, `created_at`, `handler`, `runtime`, `version`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton function version list --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function version list -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --json version,created_at
{% endraw %}{% endhighlight %}

### See also

* [maton function version](/manual/maton/function/version)
