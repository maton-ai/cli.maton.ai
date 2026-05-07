---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe subscription update

```
maton stripe subscription update <id> [flags]
```

Update a subscription. Use --items to add, replace, or
remove items in the subscription. Each --items value is a
comma-separated list of key=value pairs describing one item, where
the keys mirror Stripe's items[N][key] form fields:

  price=price_xxx              — add or replace by price
  id=si_xxx,price=price_yyy    — change an existing item's price
  id=si_xxx,quantity=3         — change quantity on an existing item
  id=si_xxx,deleted=true       — remove an existing item

Repeat --items once per item.

### Options


<dl class="flags">
	<dt>
		<code>--cancel-at-period-end &lt;string&gt;</code></dt>
	<dd>Set to &#39;true&#39; or &#39;false&#39;</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--default-payment-method &lt;string&gt;</code></dt>
	<dd>Default payment method ID</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--items &lt;stringArray&gt;</code></dt>
	<dd>Subscription item spec (key=value,key=value); repeatable, one per item</dd>

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
		<code>--proration-behavior &lt;string&gt;</code></dt>
	<dd>Proration behavior (create_prorations, none, always_invoice)</dd>

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
$ maton stripe subscription update sub_123 --metadata renewed=true
$ maton stripe subscription update sub_123 --cancel-at-period-end true
$ maton stripe subscription update sub_123 --items 'price=price_999,quantity=2'
$ maton stripe subscription update sub_123 --items 'id=si_abc,deleted=true' --items 'price=price_xyz'
$ maton stripe subscription update sub_123 --proration-behavior none
{% endraw %}{% endhighlight %}

### See also

* [maton stripe subscription](/manual/maton/stripe/subscription)
