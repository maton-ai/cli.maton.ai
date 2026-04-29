---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail message modify

Add or remove labels on a message

```
maton google-mail message modify <message-id> [flags]
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
		<code>--remove-label &lt;strings&gt;</code></dt>
	<dd>Label ID to remove (repeatable; one of --add-label/--remove-label required)</dd>

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
### Examples

{% highlight bash %}{% raw %}
$ maton google-mail message modify 18f1a2b3 --add-label STARRED
$ maton google-mail message modify 18f1a2b3 --remove-label UNREAD
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail message](./maton_google-mail_message)
