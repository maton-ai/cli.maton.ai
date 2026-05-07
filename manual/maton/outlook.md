---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook

Manage messages, folders, calendar events, and contacts in Outlook.

### Available commands

* [maton outlook calendar](/manual/maton/outlook/calendar)
* [maton outlook contact](/manual/maton/outlook/contact)
* [maton outlook event](/manual/maton/outlook/event)
* [maton outlook folder](/manual/maton/outlook/folder)
* [maton outlook message](/manual/maton/outlook/message)
* [maton outlook whoami](/manual/maton/outlook/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton outlook whoami
$ maton outlook message list --folder Inbox --top 25
$ maton outlook message send --to alice@example.com --subject hi --body "hello"
$ maton outlook event create --subject Sync --start 2026-05-10T10:00:00 --end 2026-05-10T11:00:00
$ maton outlook contact list
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
