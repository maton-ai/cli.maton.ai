---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linkedin campaign

Manage advertising campaigns (list)

### Available commands

* [maton linkedin campaign list](./maton_linkedin_campaign_list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton linkedin campaigns

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton linkedin campaign list --account-id 123456789
$ maton linkedin campaign list --account-id 123456789 --limit 50
$ maton linkedin campaigns list --account-id 123456789 --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton linkedin](./maton_linkedin)
