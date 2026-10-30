---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton bridge delete

```
maton bridge delete <bridge-id> [flags]
```

Delete a bridge by its ID. Use --yes to skip the confirmation prompt (required when running non-interactively).

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
$ maton bridge delete 3f2b9c1e-5d4a-4e8b-9a7c-1b2d3e4f5a6b
$ maton bridge delete 3f2b9c1e-5d4a-4e8b-9a7c-1b2d3e4f5a6b --yes
{% endraw %}{% endhighlight %}

### See also

* [maton bridge](/manual/maton/bridge)
