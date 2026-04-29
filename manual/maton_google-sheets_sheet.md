---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets sheet

Operate on individual sheets within a spreadsheet

### Available commands

* [maton google-sheets sheet copy](./maton_google-sheets_sheet_copy)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-sheets sheets

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-sheets sheet copy SRC --sheet-id 0 --to DST
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets](./maton_google-sheets)
