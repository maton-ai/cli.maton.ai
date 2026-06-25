---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack channel

Manage channels (list, get, create, join, invite, …)

### Available commands

* [maton slack channel archive](/manual/maton/slack/channel/archive)
* [maton slack channel create](/manual/maton/slack/channel/create)
* [maton slack channel get](/manual/maton/slack/channel/get)
* [maton slack channel invite](/manual/maton/slack/channel/invite)
* [maton slack channel join](/manual/maton/slack/channel/join)
* [maton slack channel kick](/manual/maton/slack/channel/kick)
* [maton slack channel leave](/manual/maton/slack/channel/leave)
* [maton slack channel list](/manual/maton/slack/channel/list)
* [maton slack channel mark](/manual/maton/slack/channel/mark)
* [maton slack channel members](/manual/maton/slack/channel/members)
* [maton slack channel rename](/manual/maton/slack/channel/rename)
* [maton slack channel set-purpose](/manual/maton/slack/channel/set-purpose)
* [maton slack channel set-topic](/manual/maton/slack/channel/set-topic)
* [maton slack channel unarchive](/manual/maton/slack/channel/unarchive)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack channel list
$ maton slack channel get C0123456789
$ maton slack channel create --name new-channel-name
$ maton slack channel invite C0123456789 --users U0123456789
{% endraw %}{% endhighlight %}

### See also

* [maton slack](/manual/maton/slack)
