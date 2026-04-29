---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe subscription cancel

```
maton stripe subscription cancel <id> [flags]
```

Cancel a subscription. By default the subscription is canceled
immediately (DELETE). Pass --at-period-end to instead schedule
cancellation for the end of the current billing period (POST update).

### Options


<dl class="flags">
	<dt>
		<code>--at-period-end</code></dt>
	<dd>Cancel at end of current billing period instead of immediately</dd>

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

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

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
$ maton stripe subscription cancel sub_123
$ maton stripe subscription cancel sub_123 --at-period-end
{% endraw %}{% endhighlight %}

### See also

* [maton stripe subscription](./maton_stripe_subscription)
