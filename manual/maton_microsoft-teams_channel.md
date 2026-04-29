---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams channel

Browse channels within a team

### Available commands

* [maton microsoft-teams channel list](./maton_microsoft-teams_channel_list)
* [maton microsoft-teams channel view](./maton_microsoft-teams_channel_view)


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
$ maton microsoft-teams channel view 19:chan... --team 19:abc...
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams](./maton_microsoft-teams)
