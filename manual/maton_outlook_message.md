---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook message

Read, send, and manage mailbox messages

### Available commands

* [maton outlook message delete](./maton_outlook_message_delete)
* [maton outlook message draft](./maton_outlook_message_draft)
* [maton outlook message list](./maton_outlook_message_list)
* [maton outlook message move](./maton_outlook_message_move)
* [maton outlook message reply](./maton_outlook_message_reply)
* [maton outlook message search](./maton_outlook_message_search)
* [maton outlook message send](./maton_outlook_message_send)
* [maton outlook message view](./maton_outlook_message_view)


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

* [maton outlook](./maton_outlook)
