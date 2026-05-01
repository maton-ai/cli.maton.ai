---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe refund list

List refunds

```
maton stripe refund list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--charge &lt;string&gt;</code></dt>
	<dd>Filter by charge ID</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 10)</code></dt>
	<dd>Max results per page (1-100)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--payment-intent &lt;string&gt;</code></dt>
	<dd>Filter by payment intent ID</dd>

	<dt>
		<code>--starting-after &lt;string&gt;</code></dt>
	<dd>Cursor for next page (refund ID)</dd>

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
$ maton stripe refund list
$ maton stripe refund list --charge ch_123
$ maton stripe refund list --payment-intent pi_123 --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton stripe refund](/manual/maton/stripe/refund)
