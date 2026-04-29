---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets

Manage spreadsheets and cell values in Google Sheets.

### Available commands

* [maton google-sheets sheet](./maton_google-sheets_sheet)
* [maton google-sheets spreadsheet](./maton_google-sheets_spreadsheet)
* [maton google-sheets values](./maton_google-sheets_values)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-sheets spreadsheet view <spreadsheetId>
$ maton google-sheets values get <spreadsheetId> --range 'Sheet1!A1:B10'
$ maton google-sheets values append <spreadsheetId> --range A1 --values 'Alice,100,true'
$ maton google-sheets values update <spreadsheetId> --range A1 --json-values '[["x","y"]]'
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
