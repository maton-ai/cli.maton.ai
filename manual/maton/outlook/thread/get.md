---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook thread get

```
maton outlook thread get <conversation-id> [flags]
```

List every message in a conversation across all folders, oldest first. A
message's conversationId is in "message get --json"; it stays the same when
the message moves, unlike the message ID.


### Options


<dl class="flags">
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
		<code>--select &lt;string&gt;</code></dt>
	<dd>Comma-separated fields to return (receivedDateTime is always included)</dd>

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

 maton outlook threads view, maton outlook thread view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton outlook thread get AAQkAGI...
$ maton outlook thread get AAQkAGI... --select subject,from --json
{% endraw %}{% endhighlight %}

### See also

* [maton outlook thread](/manual/maton/outlook/thread)
