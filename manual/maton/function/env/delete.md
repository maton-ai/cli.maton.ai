---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function env delete

Remove one environment variable

```
maton function env delete <key> --function <function-id> [flags]
```

### Options


<dl class="flags">
	<dt><code>-f</code>, 
		<code>--function &lt;string&gt;</code></dt>
	<dd>Function ID this resource belongs to (required)</dd>

	<dt>
		<code>--yes</code></dt>
	<dd>Skip confirmation prompt</dd>
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
$ maton function env delete GREETING --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function env delete GREETING -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --yes
{% endraw %}{% endhighlight %}

### See also

* [maton function env](/manual/maton/function/env)
