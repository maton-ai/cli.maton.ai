---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe balance-transaction

Inspect balance transactions (list, view)

### Available commands

* [maton stripe balance-transaction list](/manual/maton/stripe/balance-transaction/list)
* [maton stripe balance-transaction view](/manual/maton/stripe/balance-transaction/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe balance-transactions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe balance-transaction list
$ maton stripe balance-transaction view txn_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
