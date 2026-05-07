---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams message send

Send a message to a channel or chat

```
maton microsoft-teams message send [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Channel ID (with --team)</dd>

	<dt>
		<code>--chat &lt;string&gt;</code></dt>
	<dd>Chat ID (mutually exclusive with --team/--channel)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--html</code></dt>
	<dd>Send as HTML instead of plain text</dd>

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
		<code>--team &lt;string&gt;</code></dt>
	<dd>Team ID (with --channel)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--text &lt;string&gt;</code></dt>
	<dd>Message content (one of --text, --text-file required)</dd>

	<dt><code>-F</code>, 
		<code>--text-file &lt;string&gt;</code></dt>
	<dd>Read message text from a file path (or &#39;-&#39; for stdin)</dd>
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
$ maton microsoft-teams message send --team 19:t... --channel 19:c... --text 'hello'
$ maton microsoft-teams message send --chat 19:abc... --text 'hi'
$ maton microsoft-teams message send --chat 19:abc... --text-file ./post.md
$ maton microsoft-teams message send --chat 19:abc... --text '<b>hi</b>' --html
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams message](/manual/maton/microsoft-teams/message)
