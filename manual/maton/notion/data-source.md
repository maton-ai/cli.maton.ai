---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion data-source

Get, query, and update data sources (database schemas)

### Available commands

* [maton notion data-source get](/manual/maton/notion/data-source/get)
* [maton notion data-source query](/manual/maton/notion/data-source/query)
* [maton notion data-source update](/manual/maton/notion/data-source/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton notion ds, maton notion data-sources

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton notion data-source get 0123456789abcdef0123456789abcdef
$ maton notion data-source query <dataSourceId> --filter '{"property":"Status","select":{"equals":"Active"}}'
$ maton notion data-source update <dataSourceId> --body '{"properties":{"NewColumn":{"rich_text":{}}}}'
{% endraw %}{% endhighlight %}

### See also

* [maton notion](/manual/maton/notion)
