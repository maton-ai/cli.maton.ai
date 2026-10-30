---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton yahoo-mail draft

Create, list, get, send, and delete drafts

### Available commands

* [maton yahoo-mail draft create](/manual/maton/yahoo-mail/draft/create)
* [maton yahoo-mail draft delete](/manual/maton/yahoo-mail/draft/delete)
* [maton yahoo-mail draft get](/manual/maton/yahoo-mail/draft/get)
* [maton yahoo-mail draft list](/manual/maton/yahoo-mail/draft/list)
* [maton yahoo-mail draft send](/manual/maton/yahoo-mail/draft/send)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton yahoo-mail drafts

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton yahoo-mail draft create --to a@b.com --subject Hi --body 'Draft'
$ maton yahoo-mail draft list
$ maton yahoo-mail draft send AACBR5QM2nU9h2KG6BSRAq8VeSR
{% endraw %}{% endhighlight %}

### See also

* [maton yahoo-mail](/manual/maton/yahoo-mail)
