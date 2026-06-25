---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce record

Manage sObject records

### Available commands

* [maton salesforce record create](/manual/maton/salesforce/record/create)
* [maton salesforce record delete](/manual/maton/salesforce/record/delete)
* [maton salesforce record get](/manual/maton/salesforce/record/get)
* [maton salesforce record list](/manual/maton/salesforce/record/list)
* [maton salesforce record update](/manual/maton/salesforce/record/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton salesforce records

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton salesforce record get 0035g00000XYZ --type Contact
$ maton salesforce record list --type Contact --start 2026-04-01T00:00:00Z --end 2026-05-01T00:00:00Z
$ maton salesforce record list --recent
$ maton salesforce record create --type Contact --data '{"FirstName":"John","LastName":"Doe"}'
$ maton salesforce record update 0035g00000XYZ --type Contact --data '{"Phone":"+1234567890"}'
$ maton salesforce record delete 0035g00000A 0035g00000B
{% endraw %}{% endhighlight %}

### See also

* [maton salesforce](/manual/maton/salesforce)
