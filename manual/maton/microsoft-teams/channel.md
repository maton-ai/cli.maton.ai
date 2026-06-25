---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams channel

Browse channels within a team

### Available commands

* [maton microsoft-teams channel get](/manual/maton/microsoft-teams/channel/get)
* [maton microsoft-teams channel list](/manual/maton/microsoft-teams/channel/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton microsoft-teams channels

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton microsoft-teams team list
$ maton microsoft-teams channel list --team 19:abc...
$ maton microsoft-teams channel get 19:chan... --team 19:abc...
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams](/manual/maton/microsoft-teams)
