---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion page

View, create, update, and archive pages

### Available commands

* [maton notion page archive](./maton_notion_page_archive)
* [maton notion page create](./maton_notion_page_create)
* [maton notion page unarchive](./maton_notion_page_unarchive)
* [maton notion page update](./maton_notion_page_update)
* [maton notion page view](./maton_notion_page_view)


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
$ maton notion page view 0123456789abcdef0123456789abcdef
$ maton notion page create --parent-page 0123... --title 'Sprint planning'
$ maton notion page update 0123... --properties '{"Status":{"select":{"name":"Done"}}}'
$ maton notion page archive 0123456789abcdef0123456789abcdef
{% endraw %}{% endhighlight %}

### See also

* [maton notion](./maton_notion)
