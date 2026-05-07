---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail message reply

```
maton google-mail message reply <message-id> [flags]
```

Reply to an existing Gmail message. Threading headers (In-Reply-To, References) and the original quoted body are added automatically.

### Options


<dl class="flags">
	<dt><code>-a</code>, 
		<code>--attach &lt;stringArray&gt;</code></dt>
	<dd>Attach a file (repeatable)</dd>

	<dt>
		<code>--bcc &lt;string&gt;</code></dt>
	<dd>BCC email address(es), comma-separated</dd>

	<dt><code>-b</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Reply body (required)</dd>

	<dt>
		<code>--cc &lt;string&gt;</code></dt>
	<dd>CC email address(es), comma-separated</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--draft</code></dt>
	<dd>Save as a draft instead of sending</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--from &lt;string&gt;</code></dt>
	<dd>Sender address (for send-as alias; omit to use account default)</dd>

	<dt>
		<code>--html</code></dt>
	<dd>Treat --body as HTML (default plain text)</dd>

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
		<code>--to &lt;string&gt;</code></dt>
	<dd>Additional To email address(es), comma-separated</dd>
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
$ maton google-mail message reply 18f1a2b3 --body 'Thanks!'
$ maton google-mail message reply 18f1a2b3 --body 'Looping in Carol' --cc carol@example.com
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail message](/manual/maton/google-mail/message)
