---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe charge

Manage charges (list, get, create)

### Available commands

* [maton stripe charge create](/manual/maton/stripe/charge/create)
* [maton stripe charge get](/manual/maton/stripe/charge/get)
* [maton stripe charge list](/manual/maton/stripe/charge/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe charges

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe charge list
$ maton stripe charge get ch_123
$ maton stripe charge create --amount 1999 --currency usd --customer cus_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
