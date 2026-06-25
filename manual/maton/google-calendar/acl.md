---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar acl

Manage access control rules on a calendar

### Available commands

* [maton google-calendar acl create](/manual/maton/google-calendar/acl/create)
* [maton google-calendar acl delete](/manual/maton/google-calendar/acl/delete)
* [maton google-calendar acl get](/manual/maton/google-calendar/acl/get)
* [maton google-calendar acl list](/manual/maton/google-calendar/acl/list)
* [maton google-calendar acl update](/manual/maton/google-calendar/acl/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-calendar acls

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-calendar calendar list
$ maton google-calendar acl list -c primary
$ maton google-calendar acl create -c primary --role reader --scope alice@example.com
$ maton google-calendar acl delete user:alice@example.com -c primary
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar](/manual/maton/google-calendar)
