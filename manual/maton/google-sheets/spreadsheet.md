---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets spreadsheet

Create, get, and batch-update spreadsheets

### Available commands

* [maton google-sheets spreadsheet batch-update](/manual/maton/google-sheets/spreadsheet/batch-update)
* [maton google-sheets spreadsheet create](/manual/maton/google-sheets/spreadsheet/create)
* [maton google-sheets spreadsheet get](/manual/maton/google-sheets/spreadsheet/get)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-sheets spreadsheets

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-sheets spreadsheet get ABC
$ maton google-sheets spreadsheet create --title 'Q3 forecast'
$ maton google-sheets spreadsheet create --title 'Tracker' --sheet-title 'Issues'
$ maton google-sheets spreadsheet batch-update ABC --requests '[{"addSheet":{"properties":{"title":"Notes"}}}]'
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets](/manual/maton/google-sheets)
