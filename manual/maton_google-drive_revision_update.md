---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive revision update

```
maton google-drive revision update <revision-id> [flags]
```

Pin a revision (--keep-forever) or change its publish state. Each flag is tri-state: omit to leave the field untouched.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

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
		<code>--keep-forever</code></dt>
	<dd>Pin the revision so it isn&#39;t auto-pruned (true|false) (one of --keep-forever/--published/--publish-auto/--publish-copy)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--publish-auto</code></dt>
	<dd>Auto-publish future revisions (true|false) (one of --keep-forever/--published/--publish-auto/--publish-copy)</dd>

	<dt>
		<code>--publish-copy</code></dt>
	<dd>Publish the underlying viewers&#39; copy (true|false) (one of --keep-forever/--published/--publish-auto/--publish-copy)</dd>

	<dt>
		<code>--published</code></dt>
	<dd>Mark the revision as published (true|false) (one of --keep-forever/--published/--publish-auto/--publish-copy)</dd>

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

* [maton google-drive revision](./maton_google-drive_revision)
