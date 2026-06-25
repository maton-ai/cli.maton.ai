---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot deal

List, get, create, update, archive, and search deals

### Available commands

* [maton hubspot deal archive](/manual/maton/hubspot/deal/archive)
* [maton hubspot deal batch-archive](/manual/maton/hubspot/deal/batch-archive)
* [maton hubspot deal batch-create](/manual/maton/hubspot/deal/batch-create)
* [maton hubspot deal batch-read](/manual/maton/hubspot/deal/batch-read)
* [maton hubspot deal batch-update](/manual/maton/hubspot/deal/batch-update)
* [maton hubspot deal create](/manual/maton/hubspot/deal/create)
* [maton hubspot deal get](/manual/maton/hubspot/deal/get)
* [maton hubspot deal list](/manual/maton/hubspot/deal/list)
* [maton hubspot deal search](/manual/maton/hubspot/deal/search)
* [maton hubspot deal update](/manual/maton/hubspot/deal/update)


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
$ maton hubspot deal get 12345
$ maton hubspot deal create --set dealname='New Deal' --set amount=10000
$ maton hubspot deal search --filter dealstage:EQ:closedwon
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot](/manual/maton/hubspot)
