---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe invoice pay

Pay an invoice

```
maton stripe invoice pay <id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--forgive &lt;string&gt;</code></dt>
	<dd>Forgive remaining balance after partial payment (true/false)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--off-session &lt;string&gt;</code></dt>
	<dd>Treat as off-session (true/false)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--paid-out-of-band &lt;string&gt;</code></dt>
	<dd>Mark as paid out of band without charging (true/false)</dd>

	<dt>
		<code>--payment-method &lt;string&gt;</code></dt>
	<dd>Payment method ID to use</dd>

	<dt>
		<code>--source &lt;string&gt;</code></dt>
	<dd>Source ID (legacy)</dd>

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
$ maton stripe invoice pay in_123
$ maton stripe invoice pay in_123 --payment-method pm_456
$ maton stripe invoice pay in_123 --paid-out-of-band true
{% endraw %}{% endhighlight %}

### See also

* [maton stripe invoice](/manual/maton/stripe/invoice)
