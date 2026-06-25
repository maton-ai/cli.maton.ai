---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-docs document

Get, create, and append text to documents

### Available commands

* [maton google-docs document create](/manual/maton/google-docs/document/create)
* [maton google-docs document get](/manual/maton/google-docs/document/get)
* [maton google-docs document write](/manual/maton/google-docs/document/write)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton google-docs doc,  maton google-docs docs, maton google-docs documents

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-docs document create --title 'Sprint notes'
$ maton google-docs document get DOC_ID
$ maton google-docs document write DOC_ID --text 'Hello, world!'
$ maton google-docs document write DOC_ID -F notes.md
{% endraw %}{% endhighlight %}

### See also

* [maton google-docs](/manual/maton/google-docs)
