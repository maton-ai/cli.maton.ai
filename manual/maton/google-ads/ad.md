---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads ad

List ads

### Available commands

* [maton google-ads ad list](/manual/maton/google-ads/ad/list)


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

maton google-ads ads

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-ads ad list -c 1234567890
$ maton google-ads ad list -c 1234567890 --ad-group-id 7777
$ maton google-ads ad list -c 1234567890 --campaign-id 99999 -L 50
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads](/manual/maton/google-ads)
