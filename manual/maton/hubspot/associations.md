---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot associations

List, create, and delete CRM object links (v4 associations API)

### Available commands

* [maton hubspot associations create](/manual/maton/hubspot/associations/create)
* [maton hubspot associations delete](/manual/maton/hubspot/associations/delete)
* [maton hubspot associations list](/manual/maton/hubspot/associations/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton hubspot association

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton hubspot associations list --from contacts:12345 --to companies
$ maton hubspot associations create --from contacts:12345 --to companies:67890
$ maton hubspot associations create --from contacts:12345 --to deals:99999 --type 4
$ maton hubspot associations delete --from contacts:12345 --to companies:67890
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot](/manual/maton/hubspot)
