---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana project

List, view, create, and delete projects

### Available commands

* [maton asana project create](/manual/maton/asana/project/create)
* [maton asana project delete](/manual/maton/asana/project/delete)
* [maton asana project list](/manual/maton/asana/project/list)
* [maton asana project update](/manual/maton/asana/project/update)
* [maton asana project view](/manual/maton/asana/project/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton asana projects

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton asana workspace list
$ maton asana project list -w 12345
$ maton asana project create -w 12345 --name 'Q3 Roadmap'
$ maton asana project view 67890
{% endraw %}{% endhighlight %}

### See also

* [maton asana](/manual/maton/asana)
