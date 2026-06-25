---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion

Manage pages, databases, and blocks in Notion.

### Resource commands

* [maton notion block](/manual/maton/notion/block)
* [maton notion data-source](/manual/maton/notion/data-source)
* [maton notion database](/manual/maton/notion/database)
* [maton notion page](/manual/maton/notion/page)
* [maton notion search](/manual/maton/notion/search)
* [maton notion user](/manual/maton/notion/user)


### Auth commands

* [maton notion whoami](/manual/maton/notion/whoami)


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
$ maton notion page get 0123456789abcdef0123456789abcdef
$ maton notion data-source query <dataSourceId> --filter '{"property":"Status","select":{"equals":"Active"}}'
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
