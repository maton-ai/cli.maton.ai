---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce

Query, manage, and inspect records in Salesforce.

### Resource commands

* [maton salesforce composite](/manual/maton/salesforce/composite)
* [maton salesforce limit](/manual/maton/salesforce/limit)
* [maton salesforce object](/manual/maton/salesforce/object)
* [maton salesforce query](/manual/maton/salesforce/query)
* [maton salesforce record](/manual/maton/salesforce/record)
* [maton salesforce search](/manual/maton/salesforce/search)
* [maton salesforce version](/manual/maton/salesforce/version)


### Auth commands

* [maton salesforce whoami](/manual/maton/salesforce/whoami)


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
$ maton salesforce record create --type Contact --data '{"FirstName":"John","LastName":"Doe"}'
$ maton salesforce object describe Contact
$ maton salesforce composite call -F composite.json
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
