---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook message reply

Reply to a message

```
maton outlook message reply <message-id> [flags]
```

### Options


<dl class="flags">
	<dt><code>-t</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Reply body content (one of --body, --body-from-file required)</dd>

	<dt><code>-F</code>, 
		<code>--body-from-file &lt;string&gt;</code></dt>
	<dd>Read reply body from a file path (or &#39;-&#39; for stdin)</dd>

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
$ maton outlook message reply AAMkAGI... --body "Got it, thanks!"
$ maton outlook message reply AAMkAGI... --body-from-file ./reply.md
{% endraw %}{% endhighlight %}

### See also

* [maton outlook message](/manual/maton/outlook/message)
