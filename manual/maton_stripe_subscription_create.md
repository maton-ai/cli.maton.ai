---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe subscription create

Create a subscription for a customer

```
maton stripe subscription create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--customer &lt;string&gt;</code></dt>
	<dd>Customer ID (required)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--metadata &lt;stringArray&gt;</code></dt>
	<dd>Metadata key=value pair (repeatable)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--price &lt;string&gt;</code></dt>
	<dd>Price ID for the subscription item (required)</dd>

	<dt>
		<code>--quantity &lt;string&gt;</code></dt>
	<dd>Quantity</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--trial-days &lt;string&gt;</code></dt>
	<dd>Number of trial days</dd>
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
$ maton stripe subscription create --customer cus_123 --price price_456
$ maton stripe subscription create --customer cus_123 --price price_456 --quantity 3 --trial-days 14
{% endraw %}{% endhighlight %}

### See also

* [maton stripe subscription](./maton_stripe_subscription)
