---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot

Manage contacts, companies, and deals in HubSpot CRM.

### Available commands

* [maton hubspot associations](/manual/maton/hubspot/associations)
* [maton hubspot company](/manual/maton/hubspot/company)
* [maton hubspot contact](/manual/maton/hubspot/contact)
* [maton hubspot deal](/manual/maton/hubspot/deal)
* [maton hubspot properties](/manual/maton/hubspot/properties)
* [maton hubspot whoami](/manual/maton/hubspot/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton hubspot whoami
$ maton hubspot contact list --properties email,firstname,lastname
$ maton hubspot contact create --set email=j@ex.com --set firstname=John
$ maton hubspot deal search --filter dealstage:EQ:closedwon
$ maton hubspot associations create --from contacts:12345 --to companies:67890
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
