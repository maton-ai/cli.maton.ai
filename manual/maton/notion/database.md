---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion database

Get and create databases (use data-source for queries)

### Available commands

* [maton notion database create](/manual/maton/notion/database/create)
* [maton notion database get](/manual/maton/notion/database/get)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton notion db, maton notion databases

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton notion database get 0123456789abcdef0123456789abcdef
$ maton notion database create --parent-page 0123... --title 'Tasks'
$ maton notion database create --parent-page 0123... --title 'Tasks' --properties '{"Status":{"select":{"options":[{"name":"Active"}]}}}'
{% endraw %}{% endhighlight %}

### See also

* [maton notion](/manual/maton/notion)
