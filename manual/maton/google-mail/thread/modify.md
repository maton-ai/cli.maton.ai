---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail thread modify

Add or remove labels on every message in a thread

```
maton google-mail thread modify <thread-id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--add-label &lt;strings&gt;</code></dt>
	<dd>Label ID to add (repeatable; one of --add-label/--remove-label required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

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
		<code>--remove-label &lt;strings&gt;</code></dt>
	<dd>Label ID to remove (repeatable; one of --add-label/--remove-label required)</dd>

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
### See also

* [maton google-mail thread](/manual/maton/google-mail/thread)
