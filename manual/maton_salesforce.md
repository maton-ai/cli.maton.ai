---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce

Query, manage, and inspect records in Salesforce.

### Available commands

* [maton salesforce limits](./maton_salesforce_limits)
* [maton salesforce object](./maton_salesforce_object)
* [maton salesforce query](./maton_salesforce_query)
* [maton salesforce record](./maton_salesforce_record)
* [maton salesforce search](./maton_salesforce_search)
* [maton salesforce whoami](./maton_salesforce_whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton salesforce whoami
$ maton salesforce query 'SELECT Id,Name FROM Contact LIMIT 10'
$ maton salesforce record view 0035g00000XYZ --type Contact
$ maton salesforce record create --type Contact --data '{"FirstName":"John","LastName":"Doe"}'
$ maton salesforce object describe Contact
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
