---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot company

List, view, create, update, archive, and search companies

### Available commands

* [maton hubspot company create](/manual/maton/hubspot/company/create)
* [maton hubspot company delete](/manual/maton/hubspot/company/delete)
* [maton hubspot company list](/manual/maton/hubspot/company/list)
* [maton hubspot company search](/manual/maton/hubspot/company/search)
* [maton hubspot company update](/manual/maton/hubspot/company/update)
* [maton hubspot company view](/manual/maton/hubspot/company/view)


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

* [maton hubspot](/manual/maton/hubspot)
