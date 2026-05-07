---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe product create

Create a product

```
maton stripe product create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--active &lt;string&gt;</code></dt>
	<dd>Whether the product is active (true/false)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description shown in invoices, etc.</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--id &lt;string&gt;</code></dt>
	<dd>Custom product ID</dd>

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
	<dd>Product name (required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--shippable &lt;string&gt;</code></dt>
	<dd>Whether the product is shippable (true/false)</dd>

	<dt>
		<code>--statement-descriptor &lt;string&gt;</code></dt>
	<dd>Statement descriptor</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--unit-label &lt;string&gt;</code></dt>
	<dd>Unit label (e.g. &#39;seat&#39;, &#39;license&#39;)</dd>

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
$ maton stripe product create --name 'Pro plan'
$ maton stripe product create --name 'Widget' --id widget_v1 --description 'Acme widget' --metadata sku=W-1
{% endraw %}{% endhighlight %}

### See also

* [maton stripe product](/manual/maton/stripe/product)
