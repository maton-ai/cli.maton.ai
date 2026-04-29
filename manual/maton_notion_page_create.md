---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion page create

```
maton notion page create [flags]
```

Create a page either as a child of another page (--parent-page) or as a row in a database data source (--data-source). Exactly one parent must be specified. The --title flag is mapped to the "Name" property for database rows and the "title" property for child pages.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--data-source &lt;string&gt;</code></dt>
	<dd>Parent data source ID for database rows (one of --data-source/--parent-page)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent-page &lt;string&gt;</code></dt>
	<dd>Parent page ID for child pages (one of --data-source/--parent-page)</dd>

	<dt>
		<code>--properties &lt;string&gt;</code></dt>
	<dd>Additional properties as JSON, merged with title</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--title &lt;string&gt;</code></dt>
	<dd>Page title (required)</dd>
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
$ maton notion page create --parent-page 0123... --title 'Sprint planning'
$ maton notion page create --data-source 4567... --title 'New task' \
    --properties '{"Status":{"select":{"name":"Active"}}}'
{% endraw %}{% endhighlight %}

### See also

* [maton notion page](./maton_notion_page)
