---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack message update

Edit an existing message

```
maton slack message update [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--blocks &lt;string&gt;</code></dt>
	<dd>Replacement Block Kit blocks as a JSON array string (one of --text/--blocks)</dd>

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

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--text &lt;string&gt;</code></dt>
	<dd>New message text (one of --text/--blocks)</dd>

	<dt>
		<code>--ts &lt;string&gt;</code></dt>
	<dd>Message timestamp to edit (required)</dd>
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
$ maton slack message update --channel C012 --ts 1700000000.000100 --text 'Updated text'
{% endraw %}{% endhighlight %}

### See also

* [maton slack message](/manual/maton/slack/message)
