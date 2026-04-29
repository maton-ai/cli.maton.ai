---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar calendar

The 'list' and 'view' verbs read from the user's calendar list (calendarList resource); 'create', 'update', 'delete', and 'clear' operate on owned calendars (calendars resource). Use 'subscribe' / 'unsubscribe' to manage entries on the user's calendar list.

### Available commands

* [maton google-calendar calendar clear](./maton_google-calendar_calendar_clear)
* [maton google-calendar calendar create](./maton_google-calendar_calendar_create)
* [maton google-calendar calendar delete](./maton_google-calendar_calendar_delete)
* [maton google-calendar calendar list](./maton_google-calendar_calendar_list)
* [maton google-calendar calendar subscribe](./maton_google-calendar_calendar_subscribe)
* [maton google-calendar calendar unsubscribe](./maton_google-calendar_calendar_unsubscribe)
* [maton google-calendar calendar update](./maton_google-calendar_calendar_update)
* [maton google-calendar calendar view](./maton_google-calendar_calendar_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-calendar calendars

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-calendar calendar list
$ maton google-calendar calendar view primary
$ maton google-calendar calendar create --summary 'Project X' --timezone America/Los_Angeles
$ maton google-calendar calendar subscribe en.usa#holiday@group.v.calendar.google.com
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar](./maton_google-calendar)
