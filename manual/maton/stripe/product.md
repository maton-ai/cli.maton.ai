---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe product

Manage products (list, view, create, update, delete)

### Available commands

* [maton stripe product create](/manual/maton/stripe/product/create)
* [maton stripe product delete](/manual/maton/stripe/product/delete)
* [maton stripe product list](/manual/maton/stripe/product/list)
* [maton stripe product update](/manual/maton/stripe/product/update)
* [maton stripe product view](/manual/maton/stripe/product/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton stripe products

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton stripe product list
$ maton stripe product view prod_123
$ maton stripe product create --name 'Pro plan'
{% endraw %}{% endhighlight %}

### See also

* [maton stripe](/manual/maton/stripe)
