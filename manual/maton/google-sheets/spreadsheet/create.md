---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets spreadsheet create

```
maton google-sheets spreadsheet create [flags]
```

Create a new Google Sheets spreadsheet. Use --title for the spreadsheet name and --sheet-title to rename the implicit first sheet.

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
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--sheet-title &lt;string&gt;</code></dt>
	<dd>Title of the first sheet inside the new spreadsheet</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--title &lt;string&gt;</code></dt>
	<dd>Spreadsheet title (required)</dd>
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
$ maton google-sheets spreadsheet create --title 'Q3 forecast'
$ maton google-sheets spreadsheet create --title 'Tracker' --sheet-title 'Issues'
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets spreadsheet](/manual/maton/google-sheets/spreadsheet)
