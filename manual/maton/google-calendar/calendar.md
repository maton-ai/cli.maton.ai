---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar calendar

The 'list' and 'get' verbs read from the user's calendar list (calendarList resource); 'create', 'update', 'delete', and 'clear' operate on owned calendars (calendars resource). Use 'subscribe' / 'unsubscribe' to manage entries on the user's calendar list.

### Available commands

* [maton google-calendar calendar clear](/manual/maton/google-calendar/calendar/clear)
* [maton google-calendar calendar create](/manual/maton/google-calendar/calendar/create)
* [maton google-calendar calendar delete](/manual/maton/google-calendar/calendar/delete)
* [maton google-calendar calendar get](/manual/maton/google-calendar/calendar/get)
* [maton google-calendar calendar list](/manual/maton/google-calendar/calendar/list)
* [maton google-calendar calendar subscribe](/manual/maton/google-calendar/calendar/subscribe)
* [maton google-calendar calendar unsubscribe](/manual/maton/google-calendar/calendar/unsubscribe)
* [maton google-calendar calendar update](/manual/maton/google-calendar/calendar/update)


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
$ maton google-calendar calendar get primary
$ maton google-calendar calendar create --summary 'Project X' --timezone America/Los_Angeles
$ maton google-calendar calendar subscribe en.usa#holiday@group.v.calendar.google.com
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar](/manual/maton/google-calendar)
