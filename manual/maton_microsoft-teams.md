---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams

Manage teams, channels, and chats in Microsoft Teams.

### Available commands

* [maton microsoft-teams channel](./maton_microsoft-teams_channel)
* [maton microsoft-teams chat](./maton_microsoft-teams_chat)
* [maton microsoft-teams meeting](./maton_microsoft-teams_meeting)
* [maton microsoft-teams message](./maton_microsoft-teams_message)
* [maton microsoft-teams presence](./maton_microsoft-teams_presence)
* [maton microsoft-teams team](./maton_microsoft-teams_team)
* [maton microsoft-teams whoami](./maton_microsoft-teams_whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton microsoft-teams team list
$ maton microsoft-teams channel list --team 19:abc...
$ maton microsoft-teams message send --team 19:t... --channel 19:c... --text 'hello'
$ maton microsoft-teams chat list
$ maton microsoft-teams meeting create --subject 'Sync' --start 2026-02-18T10:00:00Z --end 2026-02-18T11:00:00Z
$ maton microsoft-teams presence get
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
