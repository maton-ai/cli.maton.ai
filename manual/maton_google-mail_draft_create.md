---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail draft create

```
maton google-mail draft create [flags]
```

Compose an RFC 5322 email and save it as a draft via users.drafts.create. The same compose pipeline as message send is used (MIME, base64url, attachments) — only the destination endpoint differs. Use draft send to dispatch the saved draft.

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
		<code>--cc &lt;string&gt;</code></dt>
	<dd>CC email address(es), comma-separated</dd>

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
		<code>--from &lt;string&gt;</code></dt>
	<dd>Sender address (for send-as alias; omit to use account default)</dd>

	<dt>
		<code>--html</code></dt>
	<dd>Treat --body as HTML (default plain text)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--subject &lt;string&gt;</code></dt>
	<dd>Email subject (required)</dd>

	<dt>
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
$ maton google-mail draft create --to alice@example.com --subject Hi --body 'Hello!'
$ maton google-mail draft create --to a@b.com --subject Files --body 'see attached' -a a.pdf
$ maton google-mail draft create --to a@b.com --subject HTML --body '<b>Hi</b>' --html
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail draft](./maton_google-mail_draft)
