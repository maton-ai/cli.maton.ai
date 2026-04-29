---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe charge create

```
maton stripe charge create [flags]
```

Create a charge against a customer or token.

Stripe recommends payment intents for new integrations; use
'maton stripe payment create' instead unless you specifically need
the legacy Charges API.

### Options


<dl class="flags">
	<dt>
		<code>--amount &lt;string&gt;</code></dt>
	<dd>Amount in cents (required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--currency &lt;string&gt;</code></dt>
	<dd>Three-letter currency code (required, e.g. usd)</dd>

	<dt>
		<code>--customer &lt;string&gt;</code></dt>
	<dd>Customer ID</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description of the charge</dd>

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
		<code>--source &lt;string&gt;</code></dt>
	<dd>Payment source (token or card ID)</dd>

	<dt>
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
$ maton stripe charge create --amount 1999 --currency usd --customer cus_123
{% endraw %}{% endhighlight %}

### See also

* [maton stripe charge](./maton_stripe_charge)
