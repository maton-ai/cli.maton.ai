---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive item move

Move an item to a new folder (and optionally rename it)

```
maton one-drive item move <item-id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dest-id &lt;string&gt;</code></dt>
	<dd>Destination folder ID (required)</dd>

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
		<code>--name &lt;string&gt;</code></dt>
	<dd>New name for the item</dd>

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
$ maton one-drive item move 01ABCDEF --dest-id 01XYZ123
$ maton one-drive item move 01ABCDEF --dest-id 01XYZ123 --name 'renamed.pdf'
{% endraw %}{% endhighlight %}

### See also

* [maton one-drive item](/manual/maton/one-drive/item)
