---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail

Manage messages, threads, and drafts in Gmail.

### Available commands

* [maton google-mail draft](./maton_google-mail_draft)
* [maton google-mail label](./maton_google-mail_label)
* [maton google-mail message](./maton_google-mail_message)
* [maton google-mail thread](./maton_google-mail_thread)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-mail message list -L 5
$ maton google-mail message view 18f1a2b3 --headers
$ maton google-mail message send --to a@b.com --subject Hi --body 'Hello!'
$ maton google-mail message reply 18f1a2b3 --body 'Got it'
$ maton google-mail label list
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
