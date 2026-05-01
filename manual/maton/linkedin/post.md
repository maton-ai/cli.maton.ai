---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linkedin post

Manage posts (list, create, delete)

### Available commands

* [maton linkedin post create](/manual/maton/linkedin/post/create)
* [maton linkedin post delete](/manual/maton/linkedin/post/delete)
* [maton linkedin post list](/manual/maton/linkedin/post/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton linkedin posts

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton linkedin post list --author urn:li:person:abc123
$ maton linkedin post list --org-id 12345
$ maton linkedin post create --author urn:li:person:abc123 --text 'Shipping today!'
$ maton linkedin post delete urn:li:share:12345
{% endraw %}{% endhighlight %}

### See also

* [maton linkedin](/manual/maton/linkedin)
