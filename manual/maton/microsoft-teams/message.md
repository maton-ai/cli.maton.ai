---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams message

Send, list, get, and reply to messages in channels and chats

### Available commands

* [maton microsoft-teams message get](/manual/maton/microsoft-teams/message/get)
* [maton microsoft-teams message list](/manual/maton/microsoft-teams/message/list)
* [maton microsoft-teams message reply](/manual/maton/microsoft-teams/message/reply)
* [maton microsoft-teams message send](/manual/maton/microsoft-teams/message/send)


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
$ maton microsoft-teams message get 1700000000000 --chat 19:abc...
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams](/manual/maton/microsoft-teams)
