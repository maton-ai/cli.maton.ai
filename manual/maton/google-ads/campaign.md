---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads campaign

List, get, and report on campaigns

### Available commands

* [maton google-ads campaign create](/manual/maton/google-ads/campaign/create)
* [maton google-ads campaign get](/manual/maton/google-ads/campaign/get)
* [maton google-ads campaign list](/manual/maton/google-ads/campaign/list)
* [maton google-ads campaign performance](/manual/maton/google-ads/campaign/performance)
* [maton google-ads campaign update](/manual/maton/google-ads/campaign/update)


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
$ maton google-ads campaign get 99999 -c 1234567890
$ maton google-ads campaign performance -c 1234567890 --date-range LAST_7_DAYS
$ maton google-ads campaign create -c 1234567890 --name "Launch" --channel SEARCH --budget-id 5555
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads](/manual/maton/google-ads)
