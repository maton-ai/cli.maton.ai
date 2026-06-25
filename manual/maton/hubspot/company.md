---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot company

List, get, create, update, archive, and search companies

### Available commands

* [maton hubspot company archive](/manual/maton/hubspot/company/archive)
* [maton hubspot company batch-archive](/manual/maton/hubspot/company/batch-archive)
* [maton hubspot company batch-create](/manual/maton/hubspot/company/batch-create)
* [maton hubspot company batch-read](/manual/maton/hubspot/company/batch-read)
* [maton hubspot company batch-update](/manual/maton/hubspot/company/batch-update)
* [maton hubspot company create](/manual/maton/hubspot/company/create)
* [maton hubspot company get](/manual/maton/hubspot/company/get)
* [maton hubspot company list](/manual/maton/hubspot/company/list)
* [maton hubspot company search](/manual/maton/hubspot/company/search)
* [maton hubspot company update](/manual/maton/hubspot/company/update)


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
$ maton hubspot company get 12345
$ maton hubspot company create --set name='Acme' --set domain='acme.com'
$ maton hubspot company search --filter name:EQ:Acme
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot](/manual/maton/hubspot)
