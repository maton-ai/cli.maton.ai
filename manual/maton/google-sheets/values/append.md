---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets values append

```
maton google-sheets values append <spreadsheet-id> [flags]
```

Append one or more rows after the last row of data in a range. Use --values for a simple comma-separated single row, or --json-values for richer payloads (single row or multi-row).

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
		<code>--include-values-in-response</code></dt>
	<dd>Echo the appended values back in the response</dd>

	<dt>
		<code>--input-option &lt;string&gt; (default &#34;USER_ENTERED&#34;)</code></dt>
	<dd>valueInputOption: USER_ENTERED or RAW</dd>

	<dt>
		<code>--insert-data-option &lt;string&gt;</code></dt>
	<dd>insertDataOption: OVERWRITE (default) or INSERT_ROWS</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json-values &lt;string&gt;</code></dt>
	<dd>JSON array (one row) or array-of-arrays (multi-row) (one of --values/--json-values)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-r</code>, 
		<code>--range &lt;string&gt;</code></dt>
	<dd>Target range in A1 notation (required)</dd>

	<dt>
		<code>--response-value-render-option &lt;string&gt;</code></dt>
	<dd>FORMATTED_VALUE (default), UNFORMATTED_VALUE, or FORMULA — applies when --include-values-in-response is set</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--values &lt;string&gt;</code></dt>
	<dd>Comma-separated cells for a single row (one of --values/--json-values)</dd>
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
$ maton google-sheets values append ABC --range A1 --values 'Alice,100,true'
$ maton google-sheets values append ABC --range Sheet2 --json-values '[["a","b"],["c","d"]]'
$ maton google-sheets values append ABC --range A1 --values 'x,y' --input-option RAW
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets values](/manual/maton/google-sheets/values)
