---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive file upload

```
maton google-drive file upload <file> [flags]
```

Upload a local file to Drive via files.create with uploadType=multipart. MIME type is detected from the extension; pass --parent to drop the file inside a specific folder, --name to override the destination filename.

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
	<dd>Override the detected MIME type</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>Target filename in Drive (defaults to source filename)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent &lt;string&gt;</code></dt>
	<dd>Parent folder ID</dd>

	<dt>
		<code>--supports-all-drives</code></dt>
	<dd>Set when uploading to a shared drive</dd>

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
$ maton google-drive file upload ./report.pdf
$ maton google-drive file upload ./report.pdf --parent 1FoLd...
$ maton google-drive file upload ./data.csv --name 'Sales Data.csv'
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive file](/manual/maton/google-drive/file)
