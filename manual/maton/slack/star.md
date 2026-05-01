---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack star

Manage stars (saved items)

### Available commands

* [maton slack star add](/manual/maton/slack/star/add)
* [maton slack star list](/manual/maton/slack/star/list)
* [maton slack star remove](/manual/maton/slack/star/remove)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton slack stars

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack star list
$ maton slack star add --channel C012 --ts 1700000000.000100
$ maton slack star remove --channel C012 --ts 1700000000.000100
{% endraw %}{% endhighlight %}

### See also

* [maton slack](/manual/maton/slack)
