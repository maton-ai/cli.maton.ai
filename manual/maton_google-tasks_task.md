---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-tasks task

List, view, create, update, complete, delete, and move tasks

### Available commands

* [maton google-tasks task complete](./maton_google-tasks_task_complete)
* [maton google-tasks task create](./maton_google-tasks_task_create)
* [maton google-tasks task delete](./maton_google-tasks_task_delete)
* [maton google-tasks task list](./maton_google-tasks_task_list)
* [maton google-tasks task move](./maton_google-tasks_task_move)
* [maton google-tasks task update](./maton_google-tasks_task_update)
* [maton google-tasks task view](./maton_google-tasks_task_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-tasks tasks

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-tasks tasklist list
$ maton google-tasks task list -l MTYxNzM4
$ maton google-tasks task create -l MTYxNzM4 --title 'Write spec'
$ maton google-tasks task complete OTQyNzc -l MTYxNzM4
{% endraw %}{% endhighlight %}

### See also

* [maton google-tasks](./maton_google-tasks)
