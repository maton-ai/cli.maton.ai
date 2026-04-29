---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce record

Manage sObject records (view, create, update, delete, recent)

### Available commands

* [maton salesforce record create](./maton_salesforce_record_create)
* [maton salesforce record delete](./maton_salesforce_record_delete)
* [maton salesforce record recent](./maton_salesforce_record_recent)
* [maton salesforce record update](./maton_salesforce_record_update)
* [maton salesforce record view](./maton_salesforce_record_view)


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
$ maton salesforce record view 0035g00000XYZ --type Contact
$ maton salesforce record create --type Contact --data '{"FirstName":"John","LastName":"Doe"}'
$ maton salesforce record update 0035g00000XYZ --type Contact --data '{"Phone":"+1234567890"}'
$ maton salesforce record recent
{% endraw %}{% endhighlight %}

### See also

* [maton salesforce](./maton_salesforce)
