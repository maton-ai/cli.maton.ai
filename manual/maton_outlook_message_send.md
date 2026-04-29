---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook message send

Send an email (builds the Microsoft Graph message object automatically)

```
maton outlook message send [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--bcc &lt;string&gt;</code></dt>
	<dd>BCC recipients, comma-separated</dd>

	<dt><code>-t</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Email body content (one of --body, --body-from-file required)</dd>

	<dt><code>-F</code>, 
		<code>--body-from-file &lt;string&gt;</code></dt>
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
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--html</code></dt>
	<dd>Send body as HTML (default: plain text)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--no-save</code></dt>
	<dd>Do not save the sent message to Sent Items</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--subject &lt;string&gt;</code></dt>
	<dd>Email subject line (required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--to &lt;string&gt;</code></dt>
	<dd>Recipient email(s), comma-separated (required)</dd>
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
$ maton outlook message send --to a@b.com --subject draft --body-from-file ./body.md
$ maton outlook message send --to a@b.com --subject draft --body "..." --no-save
{% endraw %}{% endhighlight %}

### See also

* [maton outlook message](./maton_outlook_message)
