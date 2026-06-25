---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-tasks task

List, get, create, update, complete, delete, and move tasks

### Available commands

* [maton google-tasks task complete](/manual/maton/google-tasks/task/complete)
* [maton google-tasks task create](/manual/maton/google-tasks/task/create)
* [maton google-tasks task delete](/manual/maton/google-tasks/task/delete)
* [maton google-tasks task get](/manual/maton/google-tasks/task/get)
* [maton google-tasks task list](/manual/maton/google-tasks/task/list)
* [maton google-tasks task move](/manual/maton/google-tasks/task/move)
* [maton google-tasks task update](/manual/maton/google-tasks/task/update)


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

* [maton google-tasks](/manual/maton/google-tasks)
