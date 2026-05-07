---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive file update

```
maton google-drive file update <file-id> [flags]
```

Update file metadata, parents, or binary content. Pass --metadata for arbitrary JSON and --name as a shorthand. --add-parents / --remove-parents move the file (comma-separated parent IDs). --file replaces the file's binary content; combine with --name/--metadata to update both in one request. When --file is the only thing passed, the request sends raw bytes alone and leaves existing metadata untouched. Files above 5 MiB automatically use a chunked resumable session that survives transient network errors.

### Options


<dl class="flags">
	<dt>
		<code>--add-parents &lt;string&gt;</code></dt>
	<dd>Comma-separated parent IDs to add (one of --name/--add-parents/--remove-parents/--metadata/--file)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--file &lt;string&gt;</code></dt>
	<dd>Local file whose content replaces the Drive file&#39;s binary content (one of --name/--add-parents/--remove-parents/--metadata/--file)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--metadata &lt;string&gt;</code></dt>
	<dd>Additional metadata as JSON, merged with --name (one of --name/--add-parents/--remove-parents/--metadata/--file)</dd>

	<dt>
		<code>--mime-type &lt;string&gt;</code></dt>
	<dd>Override the detected MIME type for --file</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>New filename (one of --name/--add-parents/--remove-parents/--metadata/--file)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--remove-parents &lt;string&gt;</code></dt>
	<dd>Comma-separated parent IDs to remove (one of --name/--add-parents/--remove-parents/--metadata/--file)</dd>

	<dt>
		<code>--supports-all-drives</code></dt>
	<dd>Set when the file lives in a shared drive</dd>

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
$ maton google-drive file update 1aBcD... --name 'Renamed.pdf'
$ maton google-drive file update 1aBcD... --add-parents 1NEW --remove-parents 1OLD
$ maton google-drive file update 1aBcD... --metadata '{"description":"final"}'
$ maton google-drive file update 1aBcD... --file ./report-v2.pdf
$ maton google-drive file update 1aBcD... --file ./report-v2.pdf --name 'v2.pdf'
$ maton google-drive file update 1aBcD... --file ./big.iso
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive file](/manual/maton/google-drive/file)
