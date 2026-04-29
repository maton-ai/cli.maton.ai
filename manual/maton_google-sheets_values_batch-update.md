---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets values batch-update

```
maton google-sheets values batch-update <spreadsheet-id> [flags]
```

Send a JSON array of ValueRange objects, each with "range" and "values". See https://developers.google.com/sheets/api/reference/rest/v4/spreadsheets.values/batchUpdate.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--data &lt;string&gt;</code></dt>
	<dd>JSON array of ValueRange objects (required)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--include-values-in-response</code></dt>
	<dd>Echo the written values back in the response</dd>

	<dt>
		<code>--input-option &lt;string&gt; (default &#34;USER_ENTERED&#34;)</code></dt>
	<dd>valueInputOption: USER_ENTERED or RAW</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--response-value-render-option &lt;string&gt;</code></dt>
	<dd>FORMATTED_VALUE (default), UNFORMATTED_VALUE, or FORMULA</dd>

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
$ maton google-sheets values batch-update ABC --data '[{"range":"Sheet1!A1","values":[["x"]]},{"range":"Sheet2!A1","values":[["y"]]}]'
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets values](./maton_google-sheets_values)
