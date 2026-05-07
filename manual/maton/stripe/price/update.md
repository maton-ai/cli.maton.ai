---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe price update

Update a price (most fields are immutable; active/nickname/metadata are not)

```
maton stripe price update <id> [flags]
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
		<code>--tax-behavior &lt;string&gt;</code></dt>
	<dd>Tax behavior (inclusive, exclusive, unspecified)</dd>

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
$ maton stripe price update price_123 --active false
$ maton stripe price update price_123 --nickname 'Annual plan v2'
{% endraw %}{% endhighlight %}

### See also

* [maton stripe price](/manual/maton/stripe/price)
