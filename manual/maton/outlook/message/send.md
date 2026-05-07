---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook message send

```
maton outlook message send [<draft-id>] [flags]
```

Send a message. Without a positional draft ID, builds a Microsoft Graph
message object from the compose flags and posts to /me/sendMail. With a
positional draft ID, sends an existing draft (POST /me/messages/{id}/send)
and ignores the compose flags.

### Options


<dl class="flags">
	<dt>
		<code>--bcc &lt;string&gt;</code></dt>
	<dd>BCC recipients, comma-separated</dd>

	<dt><code>-t</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Email body content (one of --body, --body-file required when composing)</dd>

	<dt><code>-F</code>, 
		<code>--body-file &lt;string&gt;</code></dt>
	<dd>Read message body from a file path (or &#39;-&#39; for stdin)</dd>

	<dt>
		<code>--cc &lt;string&gt;</code></dt>
	<dd>CC recipients, comma-separated</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--html</code></dt>
	<dd>Send body as HTML (default: plain text)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--no-save</code></dt>
	<dd>Do not save the sent message to Sent Items (compose mode only)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--subject &lt;string&gt;</code></dt>
	<dd>Email subject line (required when composing)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--to &lt;string&gt;</code></dt>
	<dd>Recipient email(s), comma-separated (required when composing)</dd>
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
$ maton outlook message send --to alice@example.com --subject "Hi" --body "hello"
$ maton outlook message send --to a@b.com,c@d.com --cc boss@b.com --subject Update --body "..."
$ maton outlook message send --to a@b.com --subject "Report" --body "<p>see attached</p>" --html
$ maton outlook message send --to a@b.com --subject draft --body-file ./body.md
$ maton outlook message send --to a@b.com --subject draft --body "..." --no-save
$ maton outlook message send AAMkAGI...   # send an existing draft
{% endraw %}{% endhighlight %}

### See also

* [maton outlook message](/manual/maton/outlook/message)
