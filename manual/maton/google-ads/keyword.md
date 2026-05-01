---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads keyword

List keywords with performance metrics

### Available commands

* [maton google-ads keyword list](/manual/maton/google-ads/keyword/list)


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

maton google-ads keywords

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-ads keyword list -c 1234567890
$ maton google-ads keyword list -c 1234567890 --date-range LAST_7_DAYS -L 25
$ maton google-ads keyword list -c 1234567890 --campaign-id 99999
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads](/manual/maton/google-ads)
