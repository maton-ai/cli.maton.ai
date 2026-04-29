---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack channel

Manage channels (list, view, create, join, invite, …)

### Available commands

* [maton slack channel archive](./maton_slack_channel_archive)
* [maton slack channel create](./maton_slack_channel_create)
* [maton slack channel invite](./maton_slack_channel_invite)
* [maton slack channel join](./maton_slack_channel_join)
* [maton slack channel kick](./maton_slack_channel_kick)
* [maton slack channel leave](./maton_slack_channel_leave)
* [maton slack channel list](./maton_slack_channel_list)
* [maton slack channel mark](./maton_slack_channel_mark)
* [maton slack channel members](./maton_slack_channel_members)
* [maton slack channel rename](./maton_slack_channel_rename)
* [maton slack channel set-purpose](./maton_slack_channel_set-purpose)
* [maton slack channel set-topic](./maton_slack_channel_set-topic)
* [maton slack channel unarchive](./maton_slack_channel_unarchive)
* [maton slack channel view](./maton_slack_channel_view)


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
$ maton slack channel view C0123456789
$ maton slack channel create --name new-channel-name
$ maton slack channel invite C0123456789 --users U0123456789
{% endraw %}{% endhighlight %}

### See also

* [maton slack](./maton_slack)
