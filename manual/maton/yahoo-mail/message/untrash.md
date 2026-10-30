---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton yahoo-mail message untrash

```
maton yahoo-mail message untrash <message-id> [flags]
```

Move a message from Trash back to INBOX, or to the folder given with --to. IMAP keeps no record of where a message was before it was trashed. The message keeps its ID; pass the folder it's now in (printed) as --folder to find it there.

### Options


<dl class="flags">
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
		<code>--folder &lt;string&gt;</code></dt>
	<dd>Folder the message is in (default the Trash folder)</dd>

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
		<code>--to &lt;string&gt; (default &#34;INBOX&#34;)</code></dt>
	<dd>Folder to move the message to</dd>
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
$ maton yahoo-mail message untrash AABFpPahntwOhfu1bXIotwdMwvD
$ maton yahoo-mail message untrash AABFpPahntwOhfu1bXIotwdMwvD --to Archive
{% endraw %}{% endhighlight %}

### See also

* [maton yahoo-mail message](/manual/maton/yahoo-mail/message)
