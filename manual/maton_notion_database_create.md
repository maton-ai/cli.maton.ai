---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion database create

```
maton notion database create [flags]
```

Create a database under --parent-page. --properties is the schema map (e.g. {"Name":{"title":{}},"Status":{"select":{"options":[{"name":"Active"}]}}}). The "Name" title property is auto-included if not present in --properties.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

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
	<dd>Parent page ID (required)</dd>

	<dt>
		<code>--properties &lt;string&gt;</code></dt>
	<dd>Schema properties as JSON object</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--title &lt;string&gt;</code></dt>
	<dd>Database title (required)</dd>
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
$ maton notion database create --parent-page 0123... --title 'Tasks' \
    --properties '{"Status":{"select":{"options":[{"name":"Active"},{"name":"Done"}]}}}'
{% endraw %}{% endhighlight %}

### See also

* [maton notion database](./maton_notion_database)
