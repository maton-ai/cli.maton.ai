---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail draft

Create, list, view, send, and delete drafts

### Available commands

* [maton google-mail draft create](/manual/maton/google-mail/draft/create)
* [maton google-mail draft delete](/manual/maton/google-mail/draft/delete)
* [maton google-mail draft list](/manual/maton/google-mail/draft/list)
* [maton google-mail draft send](/manual/maton/google-mail/draft/send)
* [maton google-mail draft view](/manual/maton/google-mail/draft/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-mail drafts

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-mail draft list
$ maton google-mail draft create --to a@b.com --subject Hi --body 'Hello!'
$ maton google-mail draft view r1234567890
$ maton google-mail draft send r1234567890
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail](/manual/maton/google-mail)
