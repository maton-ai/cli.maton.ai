---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams

Manage teams, channels, and chats in Microsoft Teams.

### Resource commands

* [maton microsoft-teams channel](/manual/maton/microsoft-teams/channel)
* [maton microsoft-teams chat](/manual/maton/microsoft-teams/chat)
* [maton microsoft-teams meeting](/manual/maton/microsoft-teams/meeting)
* [maton microsoft-teams message](/manual/maton/microsoft-teams/message)
* [maton microsoft-teams presence](/manual/maton/microsoft-teams/presence)
* [maton microsoft-teams team](/manual/maton/microsoft-teams/team)


### Auth commands

* [maton microsoft-teams whoami](/manual/maton/microsoft-teams/whoami)


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

* [maton](/manual/maton)
