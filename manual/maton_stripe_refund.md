---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe refund

Manage refunds (list, view, create)

### Available commands

* [maton stripe refund create](./maton_stripe_refund_create)
* [maton stripe refund list](./maton_stripe_refund_list)
* [maton stripe refund view](./maton_stripe_refund_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe refunds

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe refund list
$ maton stripe refund view re_123
$ maton stripe refund create --charge ch_123
$ maton stripe refund create --payment-intent pi_123 --amount 1000
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](./maton_stripe)
