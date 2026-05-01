---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive file create

```
maton google-drive file create [flags]
```

Create an empty Drive entity. Pass --mime-type 'application/vnd.google-apps.folder' for a folder, '...document' / '...spreadsheet' / '...presentation' for blank Google-native docs. To upload binary content, use 'file upload'.

### Options


<dl class="flags">
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
		<code>--mime-type &lt;string&gt;</code></dt>
	<dd>Drive MIME type (required)</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>File or folder name (required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent &lt;string&gt;</code></dt>
	<dd>Parent folder ID</dd>

	<dt>
		<code>--supports-all-drives</code></dt>
	<dd>Set when creating inside a shared drive</dd>

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
$ maton google-drive file create --name 'Q1 reports' --mime-type application/vnd.google-apps.folder
$ maton google-drive file create --name 'Notes' --mime-type application/vnd.google-apps.document --parent 1FoLd...
$ maton google-drive file create --name 'Sales' --mime-type application/vnd.google-apps.spreadsheet
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive file](/manual/maton/google-drive/file)
