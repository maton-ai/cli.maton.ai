---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe subscription

Manage subscriptions (list, view, create, update, cancel)

### Available commands

* [maton stripe subscription cancel](/manual/maton/stripe/subscription/cancel)
* [maton stripe subscription create](/manual/maton/stripe/subscription/create)
* [maton stripe subscription list](/manual/maton/stripe/subscription/list)
* [maton stripe subscription update](/manual/maton/stripe/subscription/update)
* [maton stripe subscription view](/manual/maton/stripe/subscription/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe subscriptions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe subscription list
$ maton stripe subscription view sub_123
$ maton stripe subscription create --customer cus_123 --price price_456
$ maton stripe subscription cancel sub_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
