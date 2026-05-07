---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail message view

```
maton google-mail message view <message-id> [flags]
```

Fetch a Gmail message and print its body. Defaults to plain text; use --html to print the HTML alternative when available, --headers to prepend a From/To/Cc/Subject/Date block, or --raw to dump the raw API JSON. Use --fetch-format (minimal/metadata/full/raw) and --metadata-header to control Gmail's users.messages.get query params directly — when --fetch-format is set, the raw API response is printed and body parsing is skipped.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--fetch-format &lt;string&gt;</code></dt>
	<dd>Gmail messages.get format: minimal, metadata, full, raw (forces raw JSON output)</dd>

	<dt>
		<code>--headers</code></dt>
	<dd>Print From/To/Cc/Subject/Date before the body</dd>

	<dt>
		<code>--html</code></dt>
	<dd>Print the HTML body instead of plain text</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--metadata-header &lt;strings&gt;</code></dt>
	<dd>Header to include when --fetch-format=metadata (repeatable or comma-separated, e.g. From,Subject,Date)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--raw</code></dt>
	<dd>Print the raw users.messages.get response as JSON</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>
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
$ maton google-mail message view 18f1a2b3c4d
$ maton google-mail message view 18f1a2b3c4d --headers
$ maton google-mail message view 18f1a2b3c4d --raw --json
$ maton google-mail message view 18f1a2b3c4d --fetch-format metadata --metadata-header From,Subject,Date
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail message](/manual/maton/google-mail/message)
