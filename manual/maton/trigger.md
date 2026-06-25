---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger

Work with Maton triggers that act on matching app events.

### Available commands

* [maton trigger create](/manual/maton/trigger/create)
* [maton trigger delete](/manual/maton/trigger/delete)
* [maton trigger get](/manual/maton/trigger/get)
* [maton trigger list](/manual/maton/trigger/list)
* [maton trigger update](/manual/maton/trigger/update)


### Resource commands

* [maton trigger destination](/manual/maton/trigger/destination)
* [maton trigger event](/manual/maton/trigger/event)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger list
$ maton trigger create --source github --event-type issue.opened --connection-id conn_123
$ maton trigger get <trigger-id>
$ maton trigger destination create --trigger <trigger-id> --url https://httpbin.org/post
$ maton trigger event list --trigger <trigger-id>
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
