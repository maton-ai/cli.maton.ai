---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe price

Manage prices in Stripe. The Stripe API does not support deleting
prices — set --active=false to deactivate one instead.

### Available commands

* [maton stripe price create](/manual/maton/stripe/price/create)
* [maton stripe price get](/manual/maton/stripe/price/get)
* [maton stripe price list](/manual/maton/stripe/price/list)
* [maton stripe price update](/manual/maton/stripe/price/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe prices

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe price list --product prod_123
$ maton stripe price get price_123
$ maton stripe price create --product prod_123 --currency usd --unit-amount 1999
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
