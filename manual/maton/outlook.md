---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook

Manage messages and folders in Outlook.

### Available commands

* [maton outlook folder](/manual/maton/outlook/folder)
* [maton outlook message](/manual/maton/outlook/message)
* [maton outlook whoami](/manual/maton/outlook/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton outlook message list --folder Inbox --top 25
$ maton outlook message send --to alice@example.com --subject hi --body "hello"
$ maton outlook message search "quarterly report"
$ maton outlook folder list
$ maton outlook whoami
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
