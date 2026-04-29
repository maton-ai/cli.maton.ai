---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe invoice

Manage invoices (list, view, create)

### Available commands

* [maton stripe invoice create](./maton_stripe_invoice_create)
* [maton stripe invoice list](./maton_stripe_invoice_list)
* [maton stripe invoice view](./maton_stripe_invoice_view)


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
$ maton stripe invoice view in_123
$ maton stripe invoice create --customer cus_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](./maton_stripe)
