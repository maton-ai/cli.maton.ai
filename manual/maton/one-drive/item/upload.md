---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive item upload

```
maton one-drive item upload <local-file> [flags]
```

Upload a local file to OneDrive. Files ≤4 MiB go through a single PUT to /root:/path:/content; larger files automatically open an upload session and stream in chunks. The destination path is given by --path and must include the target filename.

### Options


<dl class="flags">
	<dt>
		<code>--conflict &lt;string&gt;</code></dt>
	<dd>Conflict behavior: fail, replace, rename</dd>

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
	<dd>Override the detected Content-Type</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--path &lt;string&gt;</code></dt>
	<dd>Destination path including filename (required, e.g. Documents/report.pdf)</dd>

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
$ maton one-drive item upload ./report.pdf --path Documents/report.pdf
$ maton one-drive item upload ./data.csv --path Reports/2026/data.csv --conflict replace
{% endraw %}{% endhighlight %}

### See also

* [maton one-drive item](/manual/maton/one-drive/item)
