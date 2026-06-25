---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe invoice

Manage invoices (list, get, create, finalize, pay, void)

### Available commands

* [maton stripe invoice create](/manual/maton/stripe/invoice/create)
* [maton stripe invoice finalize](/manual/maton/stripe/invoice/finalize)
* [maton stripe invoice get](/manual/maton/stripe/invoice/get)
* [maton stripe invoice list](/manual/maton/stripe/invoice/list)
* [maton stripe invoice pay](/manual/maton/stripe/invoice/pay)
* [maton stripe invoice void](/manual/maton/stripe/invoice/void)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe invoices

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe invoice list
$ maton stripe invoice get in_123
$ maton stripe invoice create --customer cus_123
$ maton stripe invoice finalize in_123
$ maton stripe invoice pay in_123
$ maton stripe invoice void in_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
