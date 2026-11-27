---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-docs document list

```
maton google-docs document list [flags]
```

List the documents the connection can see, through Google Drive's files.list
(GET google-docs/drive/v3/files). Results are limited to documents; -Q adds a Drive
query on top (e.g. "name contains 'budget'").

With the drive.readonly scope it lists every document. With only drive.file (on by
default) it lists just the documents created or opened through Maton. To list them all,
add drive.readonly with Change permissions in the Maton console, or:
  maton connection reauthorize <connection-id> --scopes <current scopes>,https://www.googleapis.com/auth/drive.readonly


### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--corpora &lt;string&gt;</code></dt>
	<dd>Bodies to search: user, domain, drive, allDrives</dd>

	<dt>
		<code>--drive-id &lt;string&gt;</code></dt>
	<dd>Shared drive to search (implies corpora=drive)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--fields &lt;string&gt;</code></dt>
	<dd>Partial-response field mask (default: &#39;nextPageToken,files(id,name,mimeType,modifiedTime)&#39;)</dd>

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
$ maton google-docs document list
$ maton google-docs document list -Q "name contains 'budget'" --order-by 'modifiedTime desc'
$ maton google-docs document list --paginate --json
{% endraw %}{% endhighlight %}

### See also

* [maton google-docs document](/manual/maton/google-docs/document)
