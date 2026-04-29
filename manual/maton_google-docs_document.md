---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-docs document

View, create, and append text to documents

### Available commands

* [maton google-docs document create](./maton_google-docs_document_create)
* [maton google-docs document view](./maton_google-docs_document_view)
* [maton google-docs document write](./maton_google-docs_document_write)


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
$ maton google-docs document view DOC_ID
$ maton google-docs document write DOC_ID --text 'Hello, world!'
$ maton google-docs document write DOC_ID -F notes.md
{% endraw %}{% endhighlight %}

### See also

* [maton google-docs](./maton_google-docs)
