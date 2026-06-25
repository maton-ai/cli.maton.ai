---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe payment

Manage payment intents (list, get, create, confirm, cancel)

### Available commands

* [maton stripe payment cancel](/manual/maton/stripe/payment/cancel)
* [maton stripe payment confirm](/manual/maton/stripe/payment/confirm)
* [maton stripe payment create](/manual/maton/stripe/payment/create)
* [maton stripe payment get](/manual/maton/stripe/payment/get)
* [maton stripe payment list](/manual/maton/stripe/payment/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe payments

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe payment list
$ maton stripe payment get pi_123
$ maton stripe payment create --amount 1999 --currency usd
$ maton stripe payment confirm pi_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
