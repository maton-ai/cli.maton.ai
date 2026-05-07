---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe coupon create

```
maton stripe coupon create [flags]
```

Create a coupon. Provide one of --percent-off or
--amount-off (with --currency). Duration is one of 'once',
'forever', or 'repeating' (with --duration-in-months).

### Options


<dl class="flags">
	<dt>
		<code>--amount-off &lt;string&gt;</code></dt>
	<dd>Fixed-amount discount in cents (requires --currency)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--currency &lt;string&gt;</code></dt>
	<dd>Three-letter currency code (required with --amount-off)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--duration &lt;string&gt;</code></dt>
	<dd>Duration: once, forever, repeating (required)</dd>

	<dt>
		<code>--duration-in-months &lt;string&gt;</code></dt>
	<dd>Months to apply (required when --duration=repeating)</dd>

	<dt>
		<code>--id &lt;string&gt;</code></dt>
	<dd>Custom coupon ID (auto-generated if omitted)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--max-redemptions &lt;string&gt;</code></dt>
	<dd>Max times the coupon may be redeemed</dd>

	<dt>
		<code>--metadata &lt;stringArray&gt;</code></dt>
	<dd>Metadata key=value pair (repeatable)</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>Display name (shown to customers)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--percent-off &lt;string&gt;</code></dt>
	<dd>Percentage discount (1-100)</dd>

	<dt>
		<code>--redeem-by &lt;string&gt;</code></dt>
	<dd>Unix timestamp after which the coupon can no longer be redeemed</dd>

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
$ maton stripe coupon create --percent-off 25 --duration once
$ maton stripe coupon create --amount-off 500 --currency usd --duration once --id WELCOME5
$ maton stripe coupon create --percent-off 10 --duration repeating --duration-in-months 3
{% endraw %}{% endhighlight %}

### See also

* [maton stripe coupon](/manual/maton/stripe/coupon)
