---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton icloud-mail draft get

```
maton icloud-mail draft get <draft-id> [flags]
```

Fetch a draft and print its body, without marking it read. Defaults to plain text; use --html for the HTML alternative, --headers to prepend From/To/Cc/Subject/Date, or --raw for the original RFC 5322 source. With --json the output also has the folder, flags and thread_id, and message_id (the Message-ID header, which thread get also accepts).

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
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--raw</code></dt>
	<dd>Print the message&#39;s RFC 5322 source</dd>

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


### ALIASES

 maton icloud-mail drafts view, maton icloud-mail draft view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton icloud-mail draft get Drafts/3 --headers
{% endraw %}{% endhighlight %}

### See also

* [maton icloud-mail draft](/manual/maton/icloud-mail/draft)
