---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive file list

```
maton google-drive file list [flags]
```

List files visible to the connection. Use -q for Drive's query language (e.g. "mimeType='application/vnd.google-apps.folder'") or --paginate to follow nextPageToken.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--corpora &lt;string&gt;</code></dt>
	<dd>Bodies to search: user, drive, allDrives</dd>

	<dt>
		<code>--drive-id &lt;string&gt;</code></dt>
	<dd>Shared drive to search (implies corpora=drive)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--fields &lt;string&gt;</code></dt>
	<dd>Partial-response field mask (default: server default)</dd>

	<dt>
		<code>--include-items-from-all-drives</code></dt>
	<dd>Include shared drive items in results</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--order-by &lt;string&gt;</code></dt>
	<dd>Sort key, e.g. &#39;modifiedTime desc&#39;</dd>

	<dt><code>-L</code>, 
		<code>--page-size &lt;int&gt; (default 100)</code></dt>
	<dd>Max files per page (1-1000)</dd>

	<dt>
		<code>--page-token &lt;string&gt;</code></dt>
	<dd>Pagination token</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-Q</code>, 
		<code>--query &lt;q&gt;</code></dt>
	<dd>Drive query expression (the q parameter)</dd>

	<dt>
		<code>--spaces &lt;string&gt;</code></dt>
	<dd>Comma-separated spaces: drive, appDataFolder</dd>

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
$ maton google-drive file list
$ maton google-drive file list -Q "name contains 'budget'" --json
$ maton google-drive file list --drive-id 0AB... --include-items-from-all-drives --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive file](/manual/maton/google-drive/file)
