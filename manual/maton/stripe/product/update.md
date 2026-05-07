---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe product update

Update a product

```
maton stripe product update <id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--active &lt;string&gt;</code></dt>
	<dd>Active status (true/false)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--default-price &lt;string&gt;</code></dt>
	<dd>Default price ID</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description</dd>

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
		<code>--name &lt;string&gt;</code></dt>
	<dd>Product name</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--shippable &lt;string&gt;</code></dt>
	<dd>Shippable status (true/false)</dd>

	<dt>
		<code>--statement-descriptor &lt;string&gt;</code></dt>
	<dd>Statement descriptor</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--unit-label &lt;string&gt;</code></dt>
	<dd>Unit label</dd>

	<dt>
		<code>--url &lt;string&gt;</code></dt>
	<dd>Public URL of the product</dd>
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
$ maton stripe product update prod_123 --name 'New name'
$ maton stripe product update prod_123 --default-price price_456
$ maton stripe product update prod_123 --active false
{% endraw %}{% endhighlight %}

### See also

* [maton stripe product](/manual/maton/stripe/product)
