---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-tasks

Manage task lists and tasks in Google Tasks.

### Resource commands

* [maton google-tasks task](/manual/maton/google-tasks/task)
* [maton google-tasks tasklist](/manual/maton/google-tasks/tasklist)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-tasks tasklist list
$ maton google-tasks task list -l MTYxNzM4 --show-completed
$ maton google-tasks task create -l MTYxNzM4 --title 'Write spec' --due 2026-12-01
$ maton google-tasks task complete OTQyNzc -l MTYxNzM4
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
