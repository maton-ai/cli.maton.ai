---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets values get

Read values from a range

```
maton google-sheets values get <spreadsheet-id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--date-time-render-option &lt;string&gt;</code></dt>
	<dd>SERIAL_NUMBER (default for UNFORMATTED_VALUE) or FORMATTED_STRING</dd>

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
	<dd>ROWS (default) or COLUMNS — major dimension of the response</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-r</code>, 
		<code>--range &lt;string&gt;</code></dt>
	<dd>Range in A1 notation, e.g. &#39;Sheet1!A1:B2&#39; (required)</dd>

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
$ maton google-sheets values get ABC --range 'Sheet1!A1:D10'
$ maton google-sheets values get ABC --range Sheet1 --format text
$ maton google-sheets values get ABC --range A1:B2 --value-render-option UNFORMATTED_VALUE
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets values](./maton_google-sheets_values)
