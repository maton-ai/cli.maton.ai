---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function env list

List a function's environment variables

```
maton function env list --function <function-id> [flags]
```

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

 maton functions env ls, maton function env ls

### JSON Fields

`created_at`, `key`, `type`, `updated_at`, `value`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton function env list --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function env list -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --json key,type
{% endraw %}{% endhighlight %}

### See also

* [maton function env](/manual/maton/function/env)
