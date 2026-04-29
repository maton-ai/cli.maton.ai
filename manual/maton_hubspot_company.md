---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot company

List, view, create, update, archive, and search companies

### Available commands

* [maton hubspot company create](./maton_hubspot_company_create)
* [maton hubspot company delete](./maton_hubspot_company_delete)
* [maton hubspot company list](./maton_hubspot_company_list)
* [maton hubspot company search](./maton_hubspot_company_search)
* [maton hubspot company update](./maton_hubspot_company_update)
* [maton hubspot company view](./maton_hubspot_company_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton hubspot companies

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton hubspot company list
$ maton hubspot company view 12345
$ maton hubspot company create --set name='Acme' --set domain='acme.com'
$ maton hubspot company search --filter name:EQ:Acme
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot](./maton_hubspot)
