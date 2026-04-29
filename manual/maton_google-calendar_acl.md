---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar acl

Manage access control rules on a calendar

### Available commands

* [maton google-calendar acl create](./maton_google-calendar_acl_create)
* [maton google-calendar acl delete](./maton_google-calendar_acl_delete)
* [maton google-calendar acl list](./maton_google-calendar_acl_list)
* [maton google-calendar acl update](./maton_google-calendar_acl_update)
* [maton google-calendar acl view](./maton_google-calendar_acl_view)


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

* [maton google-calendar](./maton_google-calendar)
