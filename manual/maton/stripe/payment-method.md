---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe payment-method

Manage payment methods (list, get, attach, detach)

### Available commands

* [maton stripe payment-method attach](/manual/maton/stripe/payment-method/attach)
* [maton stripe payment-method detach](/manual/maton/stripe/payment-method/detach)
* [maton stripe payment-method get](/manual/maton/stripe/payment-method/get)
* [maton stripe payment-method list](/manual/maton/stripe/payment-method/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe payment-methods

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe payment-method list --customer cus_123
$ maton stripe payment-method get pm_123
$ maton stripe payment-method attach pm_123 --customer cus_123
$ maton stripe payment-method detach pm_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
