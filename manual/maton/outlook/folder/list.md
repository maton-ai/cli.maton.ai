---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook folder list

List mail folders (top-level by default; child folders with --parent)

```
maton outlook folder list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent &lt;string&gt;</code></dt>
	<dd>Parent folder ID or well-known name; lists child folders when set</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--top &lt;string&gt; (default &#34;25&#34;)</code></dt>
	<dd>OData $top — max results per page</dd>
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
$ maton outlook folder list
$ maton outlook folder list --top 100
$ maton outlook folder list --parent Inbox
$ maton outlook folder list --json
$ maton outlook folder list --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton outlook folder](/manual/maton/outlook/folder)
