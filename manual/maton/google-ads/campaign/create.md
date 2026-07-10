---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads campaign create

```
maton google-ads campaign create [flags]
```

Create a campaign by POSTing a single create operation to customers/{id}/campaigns:mutate. New campaigns default to PAUSED — pass --status ENABLED to start serving immediately.

--budget-id is the numeric campaign budget ID; the resource name is built for you (customers/{id}/campaignBudgets/{budgetId}).

A campaign always needs a bidding strategy; --bidding-strategy defaults to MANUAL_CPC. Pass another (e.g. TARGET_CPA, TARGET_ROAS) to override — TARGET_CPA additionally requires --target-cpa-micros and TARGET_ROAS requires --target-roas.


### Options


<dl class="flags">
	<dt>
		<code>--bidding-strategy &lt;string&gt; (default &#34;MANUAL_CPC&#34;)</code></dt>
	<dd>Bidding strategy: MANUAL_CPC, TARGET_CPA, TARGET_ROAS, MAXIMIZE_CONVERSIONS, etc.</dd>

	<dt>
		<code>--budget-id &lt;string&gt;</code></dt>
	<dd>Numeric campaign budget ID (required)</dd>

	<dt>
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Advertising channel type: SEARCH, DISPLAY, VIDEO, SHOPPING, PERFORMANCE_MAX, etc. (required, e.g. SEARCH/DISPLAY/PERFORMANCE_MAX)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--contains-eu-political-advertising</code></dt>
	<dd>Whether the campaign contains EU political advertising</dd>

	<dt><code>-c</code>, 
		<code>--customer-id &lt;string&gt;</code></dt>
	<dd>Google Ads customer ID (required)</dd>

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
		<code>--name &lt;string&gt;</code></dt>
	<dd>Campaign name (required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--status &lt;string&gt; (default &#34;PAUSED&#34;)</code></dt>
	<dd>Initial status: ENABLED, PAUSED</dd>

	<dt>
		<code>--target-cpa-micros &lt;int&gt; (default 0)</code></dt>
	<dd>Target CPA in micros (required for TARGET_CPA)</dd>

	<dt>
		<code>--target-roas &lt;float&gt; (default 0)</code></dt>
	<dd>Target ROAS (required for TARGET_ROAS)</dd>

	<dt><code>-t</code>, 
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


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-ads campaign create -c 1234567890 --name "Launch" --channel SEARCH --budget-id 5555
$ maton google-ads campaign create -c 1234567890 --name "Launch" --channel SEARCH --budget-id 5555 --bidding-strategy TARGET_CPA --target-cpa-micros 5000000
$ maton google-ads campaign create -c 1234567890 --name "Launch" --channel SEARCH --budget-id 5555 --status ENABLED
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads campaign](/manual/maton/google-ads/campaign)
