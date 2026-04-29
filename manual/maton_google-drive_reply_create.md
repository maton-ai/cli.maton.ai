---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive reply create

```
maton google-drive reply create [flags]
```

Add a reply to an existing comment. Use --action resolve or --action reopen to also change the comment's resolved state.

### Options


<dl class="flags">
	<dt>
		<code>--action &lt;string&gt;</code></dt>
	<dd>Optional state change: &#39;resolve&#39; or &#39;reopen&#39; (one of --content/--action)</dd>

	<dt>
		<code>--comment &lt;string&gt;</code></dt>
	<dd>Parent comment ID (required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--content &lt;string&gt;</code></dt>
	<dd>Reply text (one of --content/--action)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--fields &lt;string&gt; (default &#34;*&#34;)</code></dt>
	<dd>Partial-response field mask</dd>

	<dt><code>-f</code>, 
		<code>--file &lt;string&gt;</code></dt>
	<dd>File ID (required)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

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

* [maton google-drive reply](./maton_google-drive_reply)
