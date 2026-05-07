---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe payment create

Create a payment intent (amount in cents, e.g. 1999 = $19.99)

```
maton stripe payment create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--amount &lt;string&gt;</code></dt>
	<dd>Amount in cents (required)</dd>

	<dt>
		<code>--confirm</code></dt>
	<dd>Immediately confirm the payment intent</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--currency &lt;string&gt;</code></dt>
	<dd>Three-letter currency code (required, e.g. usd)</dd>

	<dt>
		<code>--customer &lt;string&gt;</code></dt>
	<dd>Customer ID to associate</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description of the payment</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--metadata &lt;stringArray&gt;</code></dt>
	<dd>Metadata key=value pair (repeatable)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--payment-method &lt;string&gt;</code></dt>
	<dd>Payment method ID to attach</dd>

	<dt>
		<code>--payment-method-types &lt;stringArray&gt;</code></dt>
	<dd>Allowed payment method type (e.g. card, us_bank_account); repeatable</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe payment create --amount 1999 --currency usd
$ maton stripe payment create --amount 5000 --currency usd --customer cus_123 --confirm
$ maton stripe payment create --amount 1999 --currency usd --payment-method-types card --payment-method-types us_bank_account
{% endraw %}{% endhighlight %}

### See also

* [maton stripe payment](/manual/maton/stripe/payment)
