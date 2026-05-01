---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads campaign list

List campaigns (excludes removed by default)

```
maton google-ads campaign list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-c</code>, 
		<code>--customer-id &lt;string&gt;</code></dt>
	<dd>Google Ads customer ID (required)</dd>

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
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Limit number of results (0 = no limit)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--status &lt;string&gt;</code></dt>
	<dd>Filter by status: ENABLED, PAUSED, REMOVED</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt>
		<code>--login-customer-id &lt;string&gt;</code></dt>
	<dd>Manager account ID for MCC access (forwarded as login-customer-id header)</dd>

	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton google-ads campaigns ls, maton google-ads campaign ls

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-ads campaign list -c 1234567890
$ maton google-ads campaign list -c 1234567890 --status PAUSED -L 50
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads campaign](/manual/maton/google-ads/campaign)
