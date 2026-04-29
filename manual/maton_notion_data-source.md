---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion data-source

View, query, and update data sources (database schemas)

### Available commands

* [maton notion data-source query](./maton_notion_data-source_query)
* [maton notion data-source update](./maton_notion_data-source_update)
* [maton notion data-source view](./maton_notion_data-source_view)


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
$ maton notion data-source view 0123456789abcdef0123456789abcdef
$ maton notion data-source query <dataSourceId> --filter '{"property":"Status","select":{"equals":"Active"}}'
$ maton notion data-source update <dataSourceId> --body '{"properties":{"NewColumn":{"rich_text":{}}}}'
{% endraw %}{% endhighlight %}

### See also

* [maton notion](./maton_notion)
