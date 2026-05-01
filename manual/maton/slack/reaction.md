---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack reaction

Add, remove, and inspect reactions

### Available commands

* [maton slack reaction add](/manual/maton/slack/reaction/add)
* [maton slack reaction get](/manual/maton/slack/reaction/get)
* [maton slack reaction list](/manual/maton/slack/reaction/list)
* [maton slack reaction remove](/manual/maton/slack/reaction/remove)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton slack reactions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack reaction list
$ maton slack reaction add --channel C012 --ts 1700000000.000100 --emoji thumbsup
$ maton slack reaction get --channel C012 --ts 1700000000.000100
$ maton slack reaction remove --channel C012 --ts 1700000000.000100 --emoji thumbsup
{% endraw %}{% endhighlight %}

### See also

* [maton slack](/manual/maton/slack)
