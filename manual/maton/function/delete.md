---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function delete

```
maton function delete <function-id> [flags]
```

Delete a function, its code, its versions, and its environment variables. The
URL label is released, so the function's URL stops resolving for everyone
holding it.

Use --yes to skip the confirmation prompt (required when running
non-interactively).


### Options


<dl class="flags">
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
$ maton function delete 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function delete 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --yes
{% endraw %}{% endhighlight %}

### See also

* [maton function](/manual/maton/function)
