---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar event

List, get, create, update, and delete events

### Available commands

* [maton google-calendar event create](/manual/maton/google-calendar/event/create)
* [maton google-calendar event delete](/manual/maton/google-calendar/event/delete)
* [maton google-calendar event get](/manual/maton/google-calendar/event/get)
* [maton google-calendar event import](/manual/maton/google-calendar/event/import)
* [maton google-calendar event instances](/manual/maton/google-calendar/event/instances)
* [maton google-calendar event list](/manual/maton/google-calendar/event/list)
* [maton google-calendar event move](/manual/maton/google-calendar/event/move)
* [maton google-calendar event quick-add](/manual/maton/google-calendar/event/quick-add)
* [maton google-calendar event update](/manual/maton/google-calendar/event/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-calendar events

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-calendar calendar list
$ maton google-calendar event list -c primary
$ maton google-calendar event create --summary 'Standup' --start 2026-06-17T09:00:00Z --end 2026-06-17T09:30:00Z
$ maton google-calendar event quick-add --text 'Lunch with Alice tomorrow at noon'
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar](/manual/maton/google-calendar)
