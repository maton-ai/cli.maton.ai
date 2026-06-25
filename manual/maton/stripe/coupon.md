---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe coupon

Manage coupons (list, get, create, delete)

### Available commands

* [maton stripe coupon create](/manual/maton/stripe/coupon/create)
* [maton stripe coupon delete](/manual/maton/stripe/coupon/delete)
* [maton stripe coupon get](/manual/maton/stripe/coupon/get)
* [maton stripe coupon list](/manual/maton/stripe/coupon/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe coupons

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe coupon list
$ maton stripe coupon get SUMMER25
$ maton stripe coupon create --percent-off 25 --duration once
$ maton stripe coupon delete SUMMER25
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
