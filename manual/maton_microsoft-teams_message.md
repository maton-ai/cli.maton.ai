---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams message

Send, list, view, and reply to messages in channels and chats

### Available commands

* [maton microsoft-teams message list](./maton_microsoft-teams_message_list)
* [maton microsoft-teams message reply](./maton_microsoft-teams_message_reply)
* [maton microsoft-teams message send](./maton_microsoft-teams_message_send)
* [maton microsoft-teams message view](./maton_microsoft-teams_message_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton microsoft-teams messages

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton microsoft-teams message list --chat 19:abc...
$ maton microsoft-teams message send --chat 19:abc... --text 'hi'
$ maton microsoft-teams message reply 1700000000000 --team 19:t... --channel 19:c... --text 'thanks'
$ maton microsoft-teams message view 1700000000000 --chat 19:abc...
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams](./maton_microsoft-teams)
