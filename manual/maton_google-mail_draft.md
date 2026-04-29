---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail draft

Create, list, view, send, and delete drafts

### Available commands

* [maton google-mail draft create](./maton_google-mail_draft_create)
* [maton google-mail draft delete](./maton_google-mail_draft_delete)
* [maton google-mail draft list](./maton_google-mail_draft_list)
* [maton google-mail draft send](./maton_google-mail_draft_send)
* [maton google-mail draft view](./maton_google-mail_draft_view)


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

* [maton google-mail](./maton_google-mail)
