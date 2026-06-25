---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion block

Get, list children, append, update, and delete blocks

### Available commands

* [maton notion block append](/manual/maton/notion/block/append)
* [maton notion block children](/manual/maton/notion/block/children)
* [maton notion block delete](/manual/maton/notion/block/delete)
* [maton notion block get](/manual/maton/notion/block/get)
* [maton notion block update](/manual/maton/notion/block/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton notion blocks

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton notion block get 0123456789abcdef0123456789abcdef
$ maton notion block children 0123456789abcdef0123456789abcdef
$ maton notion block append 0123... --children '[{"object":"block","type":"paragraph","paragraph":{"rich_text":[{"type":"text","text":{"content":"Hello"}}]}}]'
$ maton notion block delete 0123456789abcdef0123456789abcdef
{% endraw %}{% endhighlight %}

### See also

* [maton notion](/manual/maton/notion)
