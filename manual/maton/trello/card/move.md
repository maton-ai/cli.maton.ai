---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello card move

```
maton trello card move [flags]
```

Move every card from --from-list into --to-list. Use --to-board to
move cards across boards (the destination list must belong to that
board). To move a single card, use 'card update --list'.


### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--from-list &lt;string&gt;</code></dt>
	<dd>Source list ID (required)</dd>

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

	<dt>
		<code>--to-board &lt;string&gt;</code></dt>
	<dd>Destination board ID (defaults to the source list&#39;s board)</dd>

	<dt>
		<code>--to-list &lt;string&gt;</code></dt>
	<dd>Destination list ID (required)</dd>
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
$ maton trello card move --from-list 5f1a... --to-list 6b2c...
$ maton trello card move --from-list 5f1a... --to-list 6b2c... --to-board 7c3d...
{% endraw %}{% endhighlight %}

### See also

* [maton trello card](/manual/maton/trello/card)
