---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack

Manage messages, channels, and users in Slack.

### Available commands

* [maton slack bot](/manual/maton/slack/bot)
* [maton slack channel](/manual/maton/slack/channel)
* [maton slack conversation](/manual/maton/slack/conversation)
* [maton slack file](/manual/maton/slack/file)
* [maton slack message](/manual/maton/slack/message)
* [maton slack pin](/manual/maton/slack/pin)
* [maton slack reaction](/manual/maton/slack/reaction)
* [maton slack schedule](/manual/maton/slack/schedule)
* [maton slack search](/manual/maton/slack/search)
* [maton slack star](/manual/maton/slack/star)
* [maton slack user](/manual/maton/slack/user)
* [maton slack whoami](/manual/maton/slack/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack message send --channel C0123456789 --text 'Hello team'
$ maton slack channel list --types public_channel,private_channel
$ maton slack user lookup --email alice@example.com
$ maton slack reaction add --channel C012 --ts 1700000000.000100 --emoji thumbsup
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
