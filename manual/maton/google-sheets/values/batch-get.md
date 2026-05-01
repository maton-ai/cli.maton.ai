---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets values batch-get

Read values from multiple ranges in one call

```
maton google-sheets values batch-get <spreadsheet-id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--date-time-render-option &lt;string&gt;</code></dt>
	<dd>SERIAL_NUMBER or FORMATTED_STRING</dd>

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
		<code>--major-dimension &lt;string&gt;</code></dt>
	<dd>ROWS (default) or COLUMNS</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-r</code>, 
		<code>--range &lt;strings&gt;</code></dt>
	<dd>A1 range to read; pass repeatedly for multiple ranges (required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--value-render-option &lt;string&gt;</code></dt>
	<dd>FORMATTED_VALUE (default), UNFORMATTED_VALUE, or FORMULA</dd>
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
$ maton google-sheets values batch-get ABC --range Sheet1!A1:B2 --range Sheet2!A1
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets values](/manual/maton/google-sheets/values)
