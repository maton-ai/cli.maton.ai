---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton bridge

Work with bridges. A bridge lets Maton send requests through your network, which is useful for app connections whose provider expects a stable IP (eg. icloud-mail). To use a specific bridge, pass --bridge <bridge-id> to maton api or set the Maton-Bridge: <bridge_id> header.

### Available commands

* [maton bridge delete](/manual/maton/bridge/delete)
* [maton bridge get](/manual/maton/bridge/get)
* [maton bridge list](/manual/maton/bridge/list)
* [maton bridge update](/manual/maton/bridge/update)


### Additional commands

* [maton bridge install](/manual/maton/bridge/install)
* [maton bridge run](/manual/maton/bridge/run)
* [maton bridge status](/manual/maton/bridge/status)
* [maton bridge uninstall](/manual/maton/bridge/uninstall)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton bridge list
$ maton bridge run
$ maton bridge status
$ maton bridge install
$ maton bridge uninstall
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
