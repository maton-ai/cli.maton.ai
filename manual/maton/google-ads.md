---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads

Manage campaigns, ad groups, and ads in Google Ads.

### Available commands

* [maton google-ads account](/manual/maton/google-ads/account)
* [maton google-ads ad](/manual/maton/google-ads/ad)
* [maton google-ads ad-group](/manual/maton/google-ads/ad-group)
* [maton google-ads campaign](/manual/maton/google-ads/campaign)
* [maton google-ads keyword](/manual/maton/google-ads/keyword)
* [maton google-ads query](/manual/maton/google-ads/query)
* [maton google-ads query-stream](/manual/maton/google-ads/query-stream)


### Options


<dl class="flags">
	<dt>
		<code>--login-customer-id &lt;string&gt;</code></dt>
	<dd>Manager account ID for MCC access (forwarded as login-customer-id header)</dd>
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
$ maton google-ads account list
$ maton google-ads campaign list -c 1234567890
$ maton google-ads campaign performance -c 1234567890 --date-range LAST_7_DAYS
$ maton google-ads query -c 1234567890 --resource campaign --fields 'campaign.id, campaign.name'
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
