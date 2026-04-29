---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot deal

List, view, create, update, archive, and search deals

### Available commands

* [maton hubspot deal create](./maton_hubspot_deal_create)
* [maton hubspot deal delete](./maton_hubspot_deal_delete)
* [maton hubspot deal list](./maton_hubspot_deal_list)
* [maton hubspot deal search](./maton_hubspot_deal_search)
* [maton hubspot deal update](./maton_hubspot_deal_update)
* [maton hubspot deal view](./maton_hubspot_deal_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton hubspot deals

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton hubspot deal list
$ maton hubspot deal view 12345
$ maton hubspot deal create --set dealname='New Deal' --set amount=10000
$ maton hubspot deal search --filter dealstage:EQ:closedwon
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot](./maton_hubspot)
