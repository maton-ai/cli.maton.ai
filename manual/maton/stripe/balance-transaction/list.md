---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe balance-transaction list

List balance transactions

```
maton stripe balance-transaction list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--currency &lt;string&gt;</code></dt>
	<dd>Filter by three-letter currency code</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--ending-before &lt;string&gt;</code></dt>
	<dd>Cursor for previous page (txn ID)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 10)</code></dt>
	<dd>Max results per page (1-100)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--payout &lt;string&gt;</code></dt>
	<dd>Filter by payout ID</dd>

	<dt>
		<code>--source &lt;string&gt;</code></dt>
	<dd>Filter by source object ID (e.g. ch_123)</dd>

	<dt>
		<code>--starting-after &lt;string&gt;</code></dt>
	<dd>Cursor for next page (txn ID)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--type &lt;string&gt;</code></dt>
	<dd>Filter by transaction type (e.g. charge, refund, payout)</dd>
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
$ maton stripe balance-transaction list
$ maton stripe balance-transaction list --type charge -L 25
$ maton stripe balance-transaction list --payout po_123 --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton stripe balance-transaction](/manual/maton/stripe/balance-transaction)
