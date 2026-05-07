---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe price create

Create a price (unit-amount in cents, e.g. 1999 = $19.99)

```
maton stripe price create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--active &lt;string&gt;</code></dt>
	<dd>Whether the price is active (true/false)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--currency &lt;string&gt;</code></dt>
	<dd>Three-letter currency code (required, e.g. usd)</dd>

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
		<code>--nickname &lt;string&gt;</code></dt>
	<dd>Internal price nickname</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--product &lt;string&gt;</code></dt>
	<dd>Product ID this price belongs to (required)</dd>

	<dt>
		<code>--recurring-interval &lt;string&gt;</code></dt>
	<dd>Billing interval (day, week, month, year) — sets recurring price</dd>

	<dt>
		<code>--recurring-interval-count &lt;string&gt;</code></dt>
	<dd>Number of intervals between billings (default 1)</dd>

	<dt>
		<code>--tax-behavior &lt;string&gt;</code></dt>
	<dd>Tax behavior (inclusive, exclusive, unspecified)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--unit-amount &lt;string&gt;</code></dt>
	<dd>Unit amount in cents</dd>
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
$ maton stripe price create --product prod_123 --currency usd --unit-amount 1999
$ maton stripe price create --product prod_123 --currency usd --unit-amount 1500 --recurring-interval month
{% endraw %}{% endhighlight %}

### See also

* [maton stripe price](/manual/maton/stripe/price)
