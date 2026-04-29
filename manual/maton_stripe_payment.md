---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe payment

Manage payment intents (list, view, create, confirm, cancel)

### Available commands

* [maton stripe payment cancel](./maton_stripe_payment_cancel)
* [maton stripe payment confirm](./maton_stripe_payment_confirm)
* [maton stripe payment create](./maton_stripe_payment_create)
* [maton stripe payment list](./maton_stripe_payment_list)
* [maton stripe payment view](./maton_stripe_payment_view)


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
$ maton stripe payment view pi_123
$ maton stripe payment create --amount 1999 --currency usd
$ maton stripe payment confirm pi_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](./maton_stripe)
