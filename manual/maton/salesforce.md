---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce

Query, manage, and inspect records in Salesforce.

### Available commands

* [maton salesforce limits](/manual/maton/salesforce/limits)
* [maton salesforce object](/manual/maton/salesforce/object)
* [maton salesforce query](/manual/maton/salesforce/query)
* [maton salesforce record](/manual/maton/salesforce/record)
* [maton salesforce search](/manual/maton/salesforce/search)
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
$ maton salesforce record view 0035g00000XYZ --type Contact
$ maton salesforce record create --type Contact --data '{"FirstName":"John","LastName":"Doe"}'
$ maton salesforce object describe Contact
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
