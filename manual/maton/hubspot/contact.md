---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot contact

List, get, create, update, archive, and search contacts

### Available commands

* [maton hubspot contact archive](/manual/maton/hubspot/contact/archive)
* [maton hubspot contact batch-archive](/manual/maton/hubspot/contact/batch-archive)
* [maton hubspot contact batch-create](/manual/maton/hubspot/contact/batch-create)
* [maton hubspot contact batch-read](/manual/maton/hubspot/contact/batch-read)
* [maton hubspot contact batch-update](/manual/maton/hubspot/contact/batch-update)
* [maton hubspot contact create](/manual/maton/hubspot/contact/create)
* [maton hubspot contact gdpr-delete](/manual/maton/hubspot/contact/gdpr-delete)
* [maton hubspot contact get](/manual/maton/hubspot/contact/get)
* [maton hubspot contact list](/manual/maton/hubspot/contact/list)
* [maton hubspot contact search](/manual/maton/hubspot/contact/search)
* [maton hubspot contact update](/manual/maton/hubspot/contact/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton hubspot contacts

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton hubspot contact list
$ maton hubspot contact get 12345
$ maton hubspot contact create --set email=j@ex.com --set firstname=John
$ maton hubspot contact search --filter email:EQ:j@ex.com
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot](/manual/maton/hubspot)
