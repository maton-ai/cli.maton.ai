---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads ad-group

List ad groups

### Available commands

* [maton google-ads ad-group list](./maton_google-ads_ad-group_list)


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

 maton google-ads adgroup,  maton google-ads adgroups, maton google-ads ad-groups

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-ads ad-group list -c 1234567890
$ maton google-ads ad-group list -c 1234567890 --campaign-id 99999
$ maton google-ads ad-group list -c 1234567890 -L 25
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads](./maton_google-ads)
