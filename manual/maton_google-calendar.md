---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar

Manage calendars and events in Google Calendar.

### Available commands

* [maton google-calendar acl](./maton_google-calendar_acl)
* [maton google-calendar agenda](./maton_google-calendar_agenda)
* [maton google-calendar calendar](./maton_google-calendar_calendar)
* [maton google-calendar colors](./maton_google-calendar_colors)
* [maton google-calendar event](./maton_google-calendar_event)
* [maton google-calendar freebusy](./maton_google-calendar_freebusy)
* [maton google-calendar settings](./maton_google-calendar_settings)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-calendar agenda --today
$ maton google-calendar event create --summary 'Standup' --start 2026-06-17T09:00:00Z --end 2026-06-17T09:30:00Z
$ maton google-calendar event list -c primary --time-min 2026-06-17T00:00:00Z --time-max 2026-06-18T00:00:00Z
$ maton google-calendar calendar list
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
