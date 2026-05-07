---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton notion block update

```
maton notion block update <block-id> [flags]
```

Update a block. The --body flag is the full JSON body to PATCH (e.g. {"paragraph":{"rich_text":[...]}}).

### Options


<dl class="flags">
	<dt>
		<code>--body &lt;string&gt;</code></dt>
	<dd>Full update body as JSON (required)</dd>

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
$ maton notion block update 0123... --body '{"paragraph":{"rich_text":[{"text":{"content":"Updated"}}]}}'
{% endraw %}{% endhighlight %}

### See also

* [maton notion block](/manual/maton/notion/block)
