---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack schedule create

Schedule a message for future delivery

```
maton slack schedule create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--blocks &lt;string&gt;</code></dt>
	<dd>Block Kit blocks as a JSON array string (one of --text/--blocks)</dd>

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
		<code>--post-at &lt;int&gt; (default 0)</code></dt>
	<dd>Unix timestamp when the message should post (required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--text &lt;string&gt;</code></dt>
	<dd>Message text (one of --text/--blocks)</dd>
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
$ maton slack schedule create --channel C012 --text 'Standup in 5' --post-at 1734567890
{% endraw %}{% endhighlight %}

### See also

* [maton slack schedule](./maton_slack_schedule)
