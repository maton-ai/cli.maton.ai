---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack bookmark add

Add a bookmark to a channel

```
maton slack bookmark add [flags]
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
		<code>--emoji &lt;string&gt;</code></dt>
	<dd>Emoji shortcode (e.g. books)</dd>

	<dt>
		<code>--entity-id &lt;string&gt;</code></dt>
	<dd>Entity ID for non-link bookmarks</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--link &lt;string&gt;</code></dt>
	<dd>URL for type=link (required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent-id &lt;string&gt;</code></dt>
	<dd>Parent bookmark ID</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--title &lt;string&gt;</code></dt>
	<dd>Bookmark title (required)</dd>

	<dt>
		<code>--type &lt;string&gt; (default &#34;link&#34;)</code></dt>
	<dd>Bookmark type</dd>
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
$ maton slack bookmark add --channel C012 --title Runbook --link https://example.com/runbook
$ maton slack bookmark add --channel C012 --title Docs --link https://example.com/docs --emoji books
{% endraw %}{% endhighlight %}

### See also

* [maton slack bookmark](/manual/maton/slack/bookmark)
