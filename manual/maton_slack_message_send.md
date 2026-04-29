---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack message send

Send a message to a channel or DM

```
maton slack message send [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--blocks &lt;string&gt;</code></dt>
	<dd>Block Kit blocks as a JSON array string (one of --text/--text-from-file/--blocks)</dd>

	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Channel ID (e.g. C0123456789) (required)</dd>

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
		<code>--icon-emoji &lt;string&gt;</code></dt>
	<dd>Override the bot icon with an emoji, e.g. :ghost:</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--reply-broadcast</code></dt>
	<dd>When sent inside a thread, also broadcast to channel</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--text &lt;string&gt;</code></dt>
	<dd>Message text — supports mrkdwn (one of --text/--text-from-file/--blocks)</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;string&gt;</code></dt>
	<dd>Read message text from a file path (or &#39;-&#39; for stdin) (one of --text/--text-from-file/--blocks)</dd>

	<dt>
		<code>--unfurl-links</code></dt>
	<dd>Toggle URL link unfurling (true|false)</dd>

	<dt>
		<code>--unfurl-media</code></dt>
	<dd>Toggle media unfurling (true|false)</dd>

	<dt>
		<code>--username &lt;string&gt;</code></dt>
	<dd>Override the bot username (legacy)</dd>
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
$ maton slack message send --channel C0123456789 --text 'Deploy complete'
$ maton slack message send --channel C0123456789 --text-from-file ./post.md
$ maton slack message send --channel C012 --text 'Heads up' --blocks '[{"type":"section","text":{"type":"mrkdwn","text":"*Heads up*"}}]'
{% endraw %}{% endhighlight %}

### See also

* [maton slack message](./maton_slack_message)
