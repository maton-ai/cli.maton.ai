---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana project

List, view, create, and delete projects

### Available commands

* [maton asana project create](./maton_asana_project_create)
* [maton asana project delete](./maton_asana_project_delete)
* [maton asana project list](./maton_asana_project_list)
* [maton asana project view](./maton_asana_project_view)


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

* [maton asana](./maton_asana)
