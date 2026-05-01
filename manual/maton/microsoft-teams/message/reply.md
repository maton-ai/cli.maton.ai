---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams message reply

Reply to a channel message

```
maton microsoft-teams message reply <message-id> [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Channel ID (required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--html</code></dt>
	<dd>Send as HTML instead of plain text</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--team &lt;string&gt;</code></dt>
	<dd>Team ID (required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--text &lt;string&gt;</code></dt>
	<dd>Reply content (one of --text, --text-from-file required)</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;string&gt;</code></dt>
	<dd>Read reply text from a file path (or &#39;-&#39; for stdin)</dd>
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
$ maton microsoft-teams message reply 1700000000000 --team 19:t... --channel 19:c... --text 'thanks'
$ maton microsoft-teams message reply 1700000000000 --team 19:t... --channel 19:c... --text-from-file ./reply.md
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams message](/manual/maton/microsoft-teams/message)
