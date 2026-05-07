---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook message update

Update a message in place (mark read/unread, change subject or importance)

```
maton outlook message update <message-id> [flags]
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
		<code>--importance &lt;string&gt;</code></dt>
	<dd>Importance: low, normal, or high</dd>

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
		<code>--read</code></dt>
	<dd>Mark as read (sets isRead=true)</dd>

	<dt>
		<code>--subject &lt;string&gt;</code></dt>
	<dd>New subject line</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--unread</code></dt>
	<dd>Mark as unread (sets isRead=false)</dd>
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
$ maton outlook message update AAMkAGI... --read
$ maton outlook message update AAMkAGI... --unread
$ maton outlook message update AAMkAGI... --subject "Re: updated subject"
$ maton outlook message update AAMkAGI... --importance high
{% endraw %}{% endhighlight %}

### See also

* [maton outlook message](/manual/maton/outlook/message)
