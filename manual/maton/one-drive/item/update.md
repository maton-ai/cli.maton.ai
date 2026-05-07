---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive item update

```
maton one-drive item update <item-id> [flags]
```

Update a drive item's metadata. Pass --name to rename, --parent-id to move (sets parentReference.id), or both at once.

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
		<code>--name &lt;string&gt;</code></dt>
	<dd>New name for the item (one of --name/--parent-id)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent-id &lt;string&gt;</code></dt>
	<dd>Destination parent folder ID (one of --name/--parent-id)</dd>

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


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton one-drive item update 01ABCDEF --name renamed.pdf
$ maton one-drive item update 01ABCDEF --parent-id 01XYZ123
$ maton one-drive item update 01ABCDEF --name v2.pdf --parent-id 01XYZ123
{% endraw %}{% endhighlight %}

### See also

* [maton one-drive item](/manual/maton/one-drive/item)
