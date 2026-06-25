---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets spreadsheet get

Retrieve a spreadsheet by ID

```
maton google-sheets spreadsheet get <spreadsheet-id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--include-grid-data</code></dt>
	<dd>Include cell-level grid data in the response</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-r</code>, 
		<code>--range &lt;strings&gt;</code></dt>
	<dd>Restrict the response to one or more A1 ranges (repeatable)</dd>

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


### ALIASES

 maton google-sheets spreadsheets view, maton google-sheets spreadsheet view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-sheets spreadsheet get ABC
$ maton google-sheets spreadsheet get ABC --range 'Sheet1!A1:B2' --include-grid-data
$ maton google-sheets spreadsheet get ABC --json
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets spreadsheet](/manual/maton/google-sheets/spreadsheet)
