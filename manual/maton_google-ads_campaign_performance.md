---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads campaign performance

Get campaign performance metrics

```
maton google-ads campaign performance [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--campaign-id &lt;string&gt;</code></dt>
	<dd>Filter by campaign ID</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-c</code>, 
		<code>--customer-id &lt;string&gt;</code></dt>
	<dd>Google Ads customer ID (required)</dd>

	<dt>
		<code>--date-range &lt;string&gt; (default &#34;LAST_30_DAYS&#34;)</code></dt>
	<dd>Date range: LAST_7_DAYS, LAST_30_DAYS, THIS_MONTH, etc.</dd>

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

 maton google-ads campaigns perf, maton google-ads campaign perf

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-ads campaign performance -c 1234567890
$ maton google-ads campaign performance -c 1234567890 --date-range LAST_7_DAYS -L 5
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads campaign](./maton_google-ads_campaign)
