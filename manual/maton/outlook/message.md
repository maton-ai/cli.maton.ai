---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook message

Read, send, and manage mailbox messages

### Available commands

* [maton outlook message delete](/manual/maton/outlook/message/delete)
* [maton outlook message draft](/manual/maton/outlook/message/draft)
* [maton outlook message get](/manual/maton/outlook/message/get)
* [maton outlook message list](/manual/maton/outlook/message/list)
* [maton outlook message move](/manual/maton/outlook/message/move)
* [maton outlook message reply](/manual/maton/outlook/message/reply)
* [maton outlook message search](/manual/maton/outlook/message/search)
* [maton outlook message send](/manual/maton/outlook/message/send)
* [maton outlook message update](/manual/maton/outlook/message/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton outlook messages

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton outlook message list --folder Inbox
$ maton outlook message send --to alice@example.com --subject 'Hi' --body 'hello'
$ maton outlook message reply AAMkAGI... --body 'thanks!'
$ maton outlook message search "quarterly report"
{% endraw %}{% endhighlight %}

### See also

* [maton outlook](/manual/maton/outlook)
