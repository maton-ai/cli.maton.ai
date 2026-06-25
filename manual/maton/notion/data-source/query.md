---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion data-source query

```
maton notion data-source query <data-source-id> [flags]
```

Query a Notion data source. Use 'maton notion database get' to discover the data_source ID for a database.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--filter &lt;string&gt;</code></dt>
	<dd>Filter object as JSON</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--page-size &lt;int&gt; (default 100)</code></dt>
	<dd>Max results per page</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--sorts &lt;string&gt;</code></dt>
	<dd>Sorts array as JSON</dd>

	<dt>
		<code>--start-cursor &lt;string&gt;</code></dt>
	<dd>Pagination cursor</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>
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
$ maton notion data-source query <dataSourceId>
$ maton notion data-source query <dataSourceId> --filter '{"property":"Status","select":{"equals":"Active"}}'
$ maton notion data-source query <dataSourceId> --sorts '[{"property":"Created","direction":"descending"}]' --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton notion data-source](/manual/maton/notion/data-source)
