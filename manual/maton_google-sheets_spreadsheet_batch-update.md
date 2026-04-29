---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets spreadsheet batch-update

```
maton google-sheets spreadsheet batch-update <spreadsheet-id> [flags]
```

Send a list of Sheets batchUpdate Request objects (e.g. addSheet, deleteSheet, updateCells). The Sheets API documents the request shapes at https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets/request.

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

	<dt>
		<code>--include-spreadsheet-in-response</code></dt>
	<dd>Return the updated spreadsheet in the response</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--requests &lt;string&gt;</code></dt>
	<dd>JSON array of Sheets Request objects (required)</dd>

	<dt>
		<code>--response-include-grid-data</code></dt>
	<dd>Include cell-level grid data in the response spreadsheet</dd>

	<dt>
		<code>--response-range &lt;strings&gt;</code></dt>
	<dd>Limit the response spreadsheet to these A1 ranges (repeatable)</dd>

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
$ maton google-sheets spreadsheet batch-update ABC --requests '[{"addSheet":{"properties":{"title":"Notes"}}}]'
$ maton google-sheets spreadsheet batch-update ABC --requests "$(cat reqs.json)"
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets spreadsheet](./maton_google-sheets_spreadsheet)
