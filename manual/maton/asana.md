---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana

Manage tasks, projects, and workspaces in Asana.

### Available commands

* [maton asana project](/manual/maton/asana/project)
* [maton asana task](/manual/maton/asana/task)
* [maton asana user](/manual/maton/asana/user)
* [maton asana whoami](/manual/maton/asana/whoami)
* [maton asana workspace](/manual/maton/asana/workspace)


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

* [maton](/manual/maton)
