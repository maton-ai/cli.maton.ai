---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton yahoo-mail message list

```
maton yahoo-mail message list [flags]
```

List messages in a folder, newest first. Read-only; listing never marks a message
read. Defaults to unread messages in INBOX; pass --all to include read ones. Search
filters are combined (all must match).

The ID column is what get, reply and the other message commands take, and THREAD
is what "thread get" takes. A • marks unread messages.

Yahoo doesn't index its spam folder (Bulk) for text searches, so --subject and --text
find nothing there.


### Options


<dl class="flags">
	<dt>
		<code>--all</code></dt>
	<dd>Include read messages</dd>

	<dt>
		<code>--before &lt;string&gt;</code></dt>
	<dd>Only messages received before this date (YYYY-MM-DD)</dd>

	<dt>
		<code>--bridge &lt;string&gt;</code></dt>
	<dd>Bridge ID to send the request through (Maton-Bridge header); see &#34;maton bridge list&#34;</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--folder &lt;string&gt; (default &#34;INBOX&#34;)</code></dt>
	<dd>Folder to list (see &#34;folder list&#34;)</dd>

	<dt>
		<code>--from &lt;string&gt;</code></dt>
	<dd>Only messages whose From contains this text</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--max &lt;int&gt; (default 20)</code></dt>
	<dd>Maximum messages to show</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--since &lt;string&gt;</code></dt>
	<dd>Only messages received on or after this date (YYYY-MM-DD)</dd>

	<dt>
		<code>--subject &lt;string&gt;</code></dt>
	<dd>Only messages whose subject contains this text</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--text &lt;string&gt;</code></dt>
	<dd>Only messages whose headers or body contain this text</dd>

	<dt>
		<code>--to &lt;string&gt;</code></dt>
	<dd>Only messages whose To contains this text</dd>
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
$ maton yahoo-mail message list
$ maton yahoo-mail message list --all -L 5
$ maton yahoo-mail message list --from boss@example.com --since 2026-10-01
$ maton yahoo-mail message list --folder Sent --all --json
{% endraw %}{% endhighlight %}

### See also

* [maton yahoo-mail message](/manual/maton/yahoo-mail/message)
