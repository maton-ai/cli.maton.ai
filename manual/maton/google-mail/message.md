---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail message

List, read, send, reply to, and modify messages

### Available commands

* [maton google-mail message forward](/manual/maton/google-mail/message/forward)
* [maton google-mail message list](/manual/maton/google-mail/message/list)
* [maton google-mail message modify](/manual/maton/google-mail/message/modify)
* [maton google-mail message reply](/manual/maton/google-mail/message/reply)
* [maton google-mail message reply-all](/manual/maton/google-mail/message/reply-all)
* [maton google-mail message send](/manual/maton/google-mail/message/send)
* [maton google-mail message trash](/manual/maton/google-mail/message/trash)
* [maton google-mail message untrash](/manual/maton/google-mail/message/untrash)
* [maton google-mail message view](/manual/maton/google-mail/message/view)


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

* [maton google-mail](/manual/maton/google-mail)
