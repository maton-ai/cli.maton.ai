---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook message list

```
maton outlook message list [flags]
```

List messages from your mailbox or a specific mail folder. Without --folder all messages are returned; with --folder (name or ID, e.g. Inbox, Drafts, SentItems) only the messages in that folder are returned.

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
	<dd>OData $filter expression (e.g. &#34;isRead eq false&#34;)</dd>

	<dt>
		<code>--folder &lt;string&gt;</code></dt>
	<dd>Folder name or ID (e.g. Inbox, Drafts, SentItems)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--orderby &lt;string&gt;</code></dt>
	<dd>OData $orderby (e.g. receivedDateTime desc)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--select &lt;string&gt;</code></dt>
	<dd>Comma-separated fields (e.g. subject,from,receivedDateTime)</dd>

	<dt>
		<code>--skip &lt;string&gt;</code></dt>
	<dd>Number of results to skip (pagination)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--top &lt;string&gt; (default &#34;10&#34;)</code></dt>
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
$ maton outlook message list
$ maton outlook message list --folder Inbox --top 25
$ maton outlook message list --filter "isRead eq false" --orderby "receivedDateTime desc"
$ maton outlook message list --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton outlook message](/manual/maton/outlook/message)
