---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail message

List, read, send, reply to, and modify messages

### Available commands

* [maton google-mail message forward](./maton_google-mail_message_forward)
* [maton google-mail message list](./maton_google-mail_message_list)
* [maton google-mail message modify](./maton_google-mail_message_modify)
* [maton google-mail message reply](./maton_google-mail_message_reply)
* [maton google-mail message reply-all](./maton_google-mail_message_reply-all)
* [maton google-mail message send](./maton_google-mail_message_send)
* [maton google-mail message trash](./maton_google-mail_message_trash)
* [maton google-mail message untrash](./maton_google-mail_message_untrash)
* [maton google-mail message view](./maton_google-mail_message_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-mail messages

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-mail message list -L 5
$ maton google-mail message view 18f1a2b3 --headers
$ maton google-mail message send --to a@b.com --subject Hi --body 'Hello!'
$ maton google-mail message reply 18f1a2b3 --body 'Got it'
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail](./maton_google-mail)
