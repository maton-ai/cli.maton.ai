---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot properties

List HubSpot property definitions for an object type

### Available commands

* [maton hubspot properties list](/manual/maton/hubspot/properties/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton hubspot property

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton hubspot properties list --type contacts
$ maton hubspot properties list --type companies --archived
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot](/manual/maton/hubspot)
