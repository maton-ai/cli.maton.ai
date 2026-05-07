---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive file upload

```
maton google-drive file upload <file> [flags]
```

Upload a local file to Drive. Files above 5 MiB automatically use a chunked resumable session that survives transient network errors; smaller files use a single multipart POST. MIME type is detected from the extension; pass --parent to drop the file inside a specific folder, --name to override the destination filename (defaults to the source filename). Pass --no-metadata to skip the metadata part entirely — Drive creates the file with no name and no parent.

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
		<code>--mime-type &lt;string&gt;</code></dt>
	<dd>Override the detected MIME type</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>Target filename in Drive (defaults to source filename)</dd>

	<dt>
		<code>--no-metadata</code></dt>
	<dd>Send only file bytes (uploadType=media); Drive creates the file with no name and no parent. Conflicts with --name/--parent</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent &lt;string&gt;</code></dt>
	<dd>Parent folder ID</dd>

	<dt>
		<code>--supports-all-drives</code></dt>
	<dd>Set when uploading to a shared drive</dd>

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
$ maton google-drive file upload ./report.pdf
$ maton google-drive file upload ./report.pdf --parent 1FoLd...
$ maton google-drive file upload ./data.csv --name 'Sales Data.csv'
$ maton google-drive file upload ./blob.bin --no-metadata
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive file](/manual/maton/google-drive/file)
