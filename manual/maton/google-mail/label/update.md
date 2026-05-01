---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail label update

Update a label (PATCH — only set fields are changed)

```
maton google-mail label update <label-id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--label-list-visibility &lt;string&gt;</code></dt>
	<dd>labelShow, labelShowIfUnread, labelHide (one of --name/--label-list-visibility/--message-list-visibility required)</dd>

	<dt>
		<code>--message-list-visibility &lt;string&gt;</code></dt>
	<dd>show, hide (one of --name/--label-list-visibility/--message-list-visibility required)</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>New label name (one of --name/--label-list-visibility/--message-list-visibility required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
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
### See also

* [maton google-mail label](/manual/maton/google-mail/label)
