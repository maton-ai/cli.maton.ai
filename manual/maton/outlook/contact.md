---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook contact

Manage personal contacts

### Available commands

* [maton outlook contact create](/manual/maton/outlook/contact/create)
* [maton outlook contact delete](/manual/maton/outlook/contact/delete)
* [maton outlook contact list](/manual/maton/outlook/contact/list)
* [maton outlook contact view](/manual/maton/outlook/contact/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton outlook contacts

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton outlook contact list
$ maton outlook contact view AAMkAGI...
$ maton outlook contact create --given-name Alice --surname Smith --email alice@example.com
$ maton outlook contact delete AAMkAGI...
{% endraw %}{% endhighlight %}

### See also

* [maton outlook](/manual/maton/outlook)
