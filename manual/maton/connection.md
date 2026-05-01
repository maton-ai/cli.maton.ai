---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton connection

Work with Maton connections.

### Available commands

* [maton connection create](/manual/maton/connection/create)
* [maton connection delete](/manual/maton/connection/delete)
* [maton connection list](/manual/maton/connection/list)
* [maton connection view](/manual/maton/connection/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton connection list
$ maton connection list google-mail
$ maton connection create google-mail
$ maton connection view <connection-id>
$ maton connection delete <connection-id>
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
