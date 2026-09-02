---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function version get

```
maton function version get <version> --function <function-id> [flags]
```

Show one of a function's code versions, including the SHA-256 of its bundle,
which `version list` does not have room for.

Download the code itself with `maton function code download --version <n>`.


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

 maton function versions view,  maton functions version view,  maton functions versions view, maton function version view

### JSON Fields

`code_sha256`, `code_size`, `created_at`, `handler`, `runtime`, `version`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton function version get 2 --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function version get 2 -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --json handler,code_sha256
{% endraw %}{% endhighlight %}

### See also

* [maton function version](/manual/maton/function/version)
