---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-sheets values

Read, write, append, and clear cell ranges

### Available commands

* [maton google-sheets values append](/manual/maton/google-sheets/values/append)
* [maton google-sheets values batch-clear](/manual/maton/google-sheets/values/batch-clear)
* [maton google-sheets values batch-get](/manual/maton/google-sheets/values/batch-get)
* [maton google-sheets values batch-update](/manual/maton/google-sheets/values/batch-update)
* [maton google-sheets values clear](/manual/maton/google-sheets/values/clear)
* [maton google-sheets values get](/manual/maton/google-sheets/values/get)
* [maton google-sheets values update](/manual/maton/google-sheets/values/update)


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

* [maton google-sheets](/manual/maton/google-sheets)
