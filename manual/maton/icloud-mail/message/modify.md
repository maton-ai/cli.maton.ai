---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton icloud-mail message modify

```
maton icloud-mail message modify <message-id> [flags]
```

Mark a message read or unread, flag or unflag it, or move it to another folder (see "folder list"); several changes can be combined. IMAP mailboxes have flags and folders rather than labels. A message's ID names its folder, so moving it changes the ID; the new one is printed.

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
		<code>--flag</code></dt>
	<dd>Flag (star) the message</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--move-to &lt;string&gt;</code></dt>
	<dd>Move the message to this folder</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--read</code></dt>
	<dd>Mark as read</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--unflag</code></dt>
	<dd>Remove the flag</dd>

	<dt>
		<code>--unread</code></dt>
	<dd>Mark as unread</dd>
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
$ maton icloud-mail message modify INBOX/124 --read
$ maton icloud-mail message modify INBOX/124 --flag --move-to Archive
{% endraw %}{% endhighlight %}

### See also

* [maton icloud-mail message](/manual/maton/icloud-mail/message)
