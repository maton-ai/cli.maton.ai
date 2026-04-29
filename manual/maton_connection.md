---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton connection

Work with Maton connections.

### Available commands

* [maton connection create](./maton_connection_create)
* [maton connection delete](./maton_connection_delete)
* [maton connection list](./maton_connection_list)
* [maton connection view](./maton_connection_view)


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

* [maton](./maton)
