---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe refund create

```
maton stripe refund create [flags]
```

Refund a charge or payment intent. Exactly one of
--charge or --payment-intent must be provided. If --amount is
omitted, the full remaining amount is refunded.

### Options


<dl class="flags">
	<dt>
		<code>--amount &lt;string&gt;</code></dt>
	<dd>Amount in cents (defaults to full remaining)</dd>

	<dt>
		<code>--charge &lt;string&gt;</code></dt>
	<dd>Charge ID to refund (one of --charge or --payment-intent required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

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
		<code>--payment-intent &lt;string&gt;</code></dt>
	<dd>Payment intent ID to refund (one of --charge or --payment-intent required)</dd>

	<dt>
		<code>--reason &lt;string&gt;</code></dt>
	<dd>Reason (duplicate, fraudulent, requested_by_customer)</dd>

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
$ maton stripe refund create --charge ch_123
$ maton stripe refund create --charge ch_123 --amount 1000
$ maton stripe refund create --payment-intent pi_123 --reason requested_by_customer
{% endraw %}{% endhighlight %}

### See also

* [maton stripe refund](/manual/maton/stripe/refund)
