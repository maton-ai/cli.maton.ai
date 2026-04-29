---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets values

Read, write, append, and clear cell ranges

### Available commands

* [maton google-sheets values append](./maton_google-sheets_values_append)
* [maton google-sheets values batch-clear](./maton_google-sheets_values_batch-clear)
* [maton google-sheets values batch-get](./maton_google-sheets_values_batch-get)
* [maton google-sheets values batch-update](./maton_google-sheets_values_batch-update)
* [maton google-sheets values clear](./maton_google-sheets_values_clear)
* [maton google-sheets values get](./maton_google-sheets_values_get)
* [maton google-sheets values update](./maton_google-sheets_values_update)


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
$ maton google-sheets values append ABC --range A1 --values 'Alice,100,true'
$ maton google-sheets values update ABC --range A1 --json-values '[["x","y"]]'
$ maton google-sheets values clear ABC --range 'Sheet1!A2:D'
{% endraw %}{% endhighlight %}

### See also

* [maton google-sheets](./maton_google-sheets)
