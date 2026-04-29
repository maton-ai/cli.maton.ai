---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana

Manage tasks, projects, and workspaces in Asana.

### Available commands

* [maton asana project](./maton_asana_project)
* [maton asana task](./maton_asana_task)
* [maton asana user](./maton_asana_user)
* [maton asana whoami](./maton_asana_whoami)
* [maton asana workspace](./maton_asana_workspace)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton asana whoami
$ maton asana workspace list
$ maton asana project list --workspace 12345
$ maton asana task create --name 'Write spec' --projects 67890
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
