---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion

Manage pages, databases, and blocks in Notion.

### Available commands

* [maton notion block](./maton_notion_block)
* [maton notion data-source](./maton_notion_data-source)
* [maton notion database](./maton_notion_database)
* [maton notion page](./maton_notion_page)
* [maton notion search](./maton_notion_search)
* [maton notion user](./maton_notion_user)
* [maton notion whoami](./maton_notion_whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton notion whoami
$ maton notion search 'roadmap'
$ maton notion page view 0123456789abcdef0123456789abcdef
$ maton notion data-source query <dataSourceId> --filter '{"property":"Status","select":{"equals":"Active"}}'
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
