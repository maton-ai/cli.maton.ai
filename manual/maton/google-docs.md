---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-docs

Create, read, and append documents in Google Docs.

### Available commands

* [maton google-docs document](/manual/maton/google-docs/document)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-docs document create --title 'Sprint notes'
$ maton google-docs document view DOC_ID
$ maton google-docs document write DOC_ID --text 'Hello!'
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
