---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton icloud-mail message

List, read, send, reply to, and organise messages

### Available commands

* [maton icloud-mail message forward](/manual/maton/icloud-mail/message/forward)
* [maton icloud-mail message get](/manual/maton/icloud-mail/message/get)
* [maton icloud-mail message list](/manual/maton/icloud-mail/message/list)
* [maton icloud-mail message modify](/manual/maton/icloud-mail/message/modify)
* [maton icloud-mail message reply](/manual/maton/icloud-mail/message/reply)
* [maton icloud-mail message reply-all](/manual/maton/icloud-mail/message/reply-all)
* [maton icloud-mail message send](/manual/maton/icloud-mail/message/send)
* [maton icloud-mail message trash](/manual/maton/icloud-mail/message/trash)
* [maton icloud-mail message untrash](/manual/maton/icloud-mail/message/untrash)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton icloud-mail messages

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton icloud-mail message list -L 5
$ maton icloud-mail message get INBOX/124 --headers
$ maton icloud-mail message send --to a@b.com --subject Hi --body 'Hello!'
$ maton icloud-mail message reply INBOX/124 --body 'Got it'
{% endraw %}{% endhighlight %}

### See also

* [maton icloud-mail](/manual/maton/icloud-mail)
