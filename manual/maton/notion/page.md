---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion page

Get, create, update, and archive pages

### Available commands

* [maton notion page archive](/manual/maton/notion/page/archive)
* [maton notion page create](/manual/maton/notion/page/create)
* [maton notion page get](/manual/maton/notion/page/get)
* [maton notion page unarchive](/manual/maton/notion/page/unarchive)
* [maton notion page update](/manual/maton/notion/page/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton notion pages

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton notion page get 0123456789abcdef0123456789abcdef
$ maton notion page create --parent-page 0123... --title 'Sprint planning'
$ maton notion page update 0123... --properties '{"Status":{"select":{"name":"Done"}}}'
$ maton notion page update 0123... --icon 🚀
$ maton notion page archive 0123456789abcdef0123456789abcdef
{% endraw %}{% endhighlight %}

### See also

* [maton notion](/manual/maton/notion)
