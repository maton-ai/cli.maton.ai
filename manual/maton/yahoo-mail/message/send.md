---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton yahoo-mail message send

```
maton yahoo-mail message send [flags]
```

Compose an email and send it from the connection's mailbox. Yahoo Mail files its own copy in the Sent folder, usually within seconds but sometimes half a minute later; the output has no ID, so find the copy with "message list --folder Sent". To save without sending, use draft create.

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
	<dd>Email body — plain text (or HTML with --html) (required)</dd>

	<dt>
		<code>--bridge &lt;string&gt;</code></dt>
	<dd>Bridge ID to send the request through (Maton-Bridge header); see &#34;maton bridge list&#34;</dd>

	<dt>
		<code>--cc &lt;string&gt;</code></dt>
	<dd>CC email address(es), comma-separated</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

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

	<dt>
		<code>--subject &lt;string&gt;</code></dt>
	<dd>Email subject (required)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--to &lt;string&gt;</code></dt>
	<dd>Recipient email address(es), comma-separated (required)</dd>
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
$ maton yahoo-mail message send --to alice@example.com --subject Hi --body 'Hello!'
$ maton yahoo-mail message send --to a@b.com --subject Files --body 'see attached' -a a.pdf
{% endraw %}{% endhighlight %}

### See also

* [maton yahoo-mail message](/manual/maton/yahoo-mail/message)
