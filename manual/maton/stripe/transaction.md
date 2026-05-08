---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe transaction

Inspect balance transactions (list, view)

### Available commands

* [maton stripe transaction list](/manual/maton/stripe/transaction/list)
* [maton stripe transaction view](/manual/maton/stripe/transaction/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton stripe balance-transaction,  maton stripe balance-transactions, maton stripe transactions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe transaction list
$ maton stripe transaction view txn_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
