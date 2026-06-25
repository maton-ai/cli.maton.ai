---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive item get

```
maton one-drive item get [<item-id>] [flags]
```

Show metadata for a drive item. Pass an item ID, the literal "root" for the drive root (/me/drive/root), or --special <name> for a well-known folder (documents, photos, cameraroll, approot, music).

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--expand &lt;string&gt;</code></dt>
	<dd>Relationships to expand ($expand), e.g. children,thumbnails</dd>

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
	<dd>Comma-separated fields ($select)</dd>

	<dt>
		<code>--special &lt;string&gt;</code></dt>
	<dd>Well-known folder name: documents, photos, cameraroll, approot, music</dd>

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

 maton one-drive items view, maton one-drive item view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton one-drive item get 01ABCDEF
$ maton one-drive item get 01ABCDEF --expand children
$ maton one-drive item get root
$ maton one-drive item get --special documents
{% endraw %}{% endhighlight %}

### See also

* [maton one-drive item](/manual/maton/one-drive/item)
