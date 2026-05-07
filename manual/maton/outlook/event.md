---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook event

Manage calendar events

### Available commands

* [maton outlook event create](/manual/maton/outlook/event/create)
* [maton outlook event delete](/manual/maton/outlook/event/delete)
* [maton outlook event list](/manual/maton/outlook/event/list)
* [maton outlook event view](/manual/maton/outlook/event/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton outlook events

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton outlook event list --filter "start/dateTime ge '2026-01-01'"
$ maton outlook event create --subject Sync --start 2026-05-10T10:00:00 --end 2026-05-10T11:00:00
$ maton outlook event view AAMkAGI...
$ maton outlook event delete AAMkAGI...
{% endraw %}{% endhighlight %}

### See also

* [maton outlook](/manual/maton/outlook)
