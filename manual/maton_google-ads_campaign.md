---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads campaign

List, view, and report on campaigns

### Available commands

* [maton google-ads campaign create](./maton_google-ads_campaign_create)
* [maton google-ads campaign list](./maton_google-ads_campaign_list)
* [maton google-ads campaign performance](./maton_google-ads_campaign_performance)
* [maton google-ads campaign update](./maton_google-ads_campaign_update)
* [maton google-ads campaign view](./maton_google-ads_campaign_view)


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

maton google-ads campaigns

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-ads campaign list -c 1234567890
$ maton google-ads campaign view 99999 -c 1234567890
$ maton google-ads campaign performance -c 1234567890 --date-range LAST_7_DAYS
$ maton google-ads campaign create -c 1234567890 --name "Launch" --channel SEARCH --budget-id 5555
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads](./maton_google-ads)
