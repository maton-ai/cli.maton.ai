---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar event

List, view, create, update, and delete events

### Available commands

* [maton google-calendar event create](./maton_google-calendar_event_create)
* [maton google-calendar event delete](./maton_google-calendar_event_delete)
* [maton google-calendar event import](./maton_google-calendar_event_import)
* [maton google-calendar event instances](./maton_google-calendar_event_instances)
* [maton google-calendar event list](./maton_google-calendar_event_list)
* [maton google-calendar event move](./maton_google-calendar_event_move)
* [maton google-calendar event quick-add](./maton_google-calendar_event_quick-add)
* [maton google-calendar event update](./maton_google-calendar_event_update)
* [maton google-calendar event view](./maton_google-calendar_event_view)


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

* [maton google-calendar](./maton_google-calendar)
