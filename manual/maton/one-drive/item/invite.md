---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive item invite

```
maton one-drive item invite <item-id> [flags]
```

Grant access to a drive item for one or more email recipients. --emails accepts a comma-separated list. --roles is a comma-separated list of "read" and/or "write" (default "read"). When --send-invitation is true (the default) an email is sent to each recipient.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--emails &lt;string&gt;</code></dt>
	<dd>Comma-separated recipient emails (required)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--message &lt;string&gt;</code></dt>
	<dd>Optional message included in the invitation email</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--require-sign-in (default true)</code></dt>
	<dd>Recipients must sign in to access the item</dd>

	<dt>
		<code>--roles &lt;string&gt; (default &#34;read&#34;)</code></dt>
	<dd>Comma-separated roles: read, write</dd>

	<dt>
		<code>--send-invitation (default true)</code></dt>
	<dd>Send an email notification to each recipient</dd>

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
$ maton one-drive item invite 01ABCDEF --emails alice@example.com
$ maton one-drive item invite 01ABCDEF --emails alice@example.com,bob@example.com --roles write
$ maton one-drive item invite 01ABCDEF --emails alice@example.com --message 'Have a look' --require-sign-in=false
{% endraw %}{% endhighlight %}

### See also

* [maton one-drive item](/manual/maton/one-drive/item)
