---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe

Manage customers, payments, and subscriptions in Stripe.

### Available commands

* [maton stripe balance](/manual/maton/stripe/balance)
* [maton stripe charge](/manual/maton/stripe/charge)
* [maton stripe customer](/manual/maton/stripe/customer)
* [maton stripe invoice](/manual/maton/stripe/invoice)
* [maton stripe payment](/manual/maton/stripe/payment)
* [maton stripe refund](/manual/maton/stripe/refund)
* [maton stripe subscription](/manual/maton/stripe/subscription)
* [maton stripe whoami](/manual/maton/stripe/whoami)


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

* [maton](/manual/maton)
