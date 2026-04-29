---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe

Manage customers, payments, and subscriptions in Stripe.

### Available commands

* [maton stripe balance](./maton_stripe_balance)
* [maton stripe charge](./maton_stripe_charge)
* [maton stripe customer](./maton_stripe_customer)
* [maton stripe invoice](./maton_stripe_invoice)
* [maton stripe payment](./maton_stripe_payment)
* [maton stripe refund](./maton_stripe_refund)
* [maton stripe subscription](./maton_stripe_subscription)
* [maton stripe whoami](./maton_stripe_whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe whoami
$ maton stripe balance
$ maton stripe customer list -L 5
$ maton stripe payment create --amount 1999 --currency usd --customer cus_123
$ maton stripe subscription cancel sub_123 --at-period-end
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
