---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams meeting

Schedule online meetings

### Available commands

* [maton microsoft-teams meeting create](/manual/maton/microsoft-teams/meeting/create)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton microsoft-teams meetings

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton microsoft-teams meeting create --subject 'Team Sync' --start 2026-02-18T10:00:00Z --end 2026-02-18T11:00:00Z
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams](/manual/maton/microsoft-teams)
