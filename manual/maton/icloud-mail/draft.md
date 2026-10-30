---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton icloud-mail draft

Create, list, get, send, and delete drafts

### Available commands

* [maton icloud-mail draft create](/manual/maton/icloud-mail/draft/create)
* [maton icloud-mail draft delete](/manual/maton/icloud-mail/draft/delete)
* [maton icloud-mail draft get](/manual/maton/icloud-mail/draft/get)
* [maton icloud-mail draft list](/manual/maton/icloud-mail/draft/list)
* [maton icloud-mail draft send](/manual/maton/icloud-mail/draft/send)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton icloud-mail drafts

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton icloud-mail draft create --to a@b.com --subject Hi --body 'Draft'
$ maton icloud-mail draft list
$ maton icloud-mail draft send Drafts/3
{% endraw %}{% endhighlight %}

### See also

* [maton icloud-mail](/manual/maton/icloud-mail)
