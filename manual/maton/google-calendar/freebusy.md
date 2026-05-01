---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar freebusy

Free/busy queries across calendars

### Available commands

* [maton google-calendar freebusy query](/manual/maton/google-calendar/freebusy/query)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-calendar calendar list
$ maton google-calendar freebusy query --time-min 2026-06-17T00:00:00Z --time-max 2026-06-18T00:00:00Z --calendar primary
$ maton google-calendar freebusy query --time-min 2026-06-17T00:00:00Z --time-max 2026-06-18T00:00:00Z --calendar primary --calendar work@example.com
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar](/manual/maton/google-calendar)
