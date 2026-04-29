---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-tasks tasklist

List, view, create, update, and delete task lists

### Available commands

* [maton google-tasks tasklist clear](./maton_google-tasks_tasklist_clear)
* [maton google-tasks tasklist create](./maton_google-tasks_tasklist_create)
* [maton google-tasks tasklist delete](./maton_google-tasks_tasklist_delete)
* [maton google-tasks tasklist list](./maton_google-tasks_tasklist_list)
* [maton google-tasks tasklist update](./maton_google-tasks_tasklist_update)
* [maton google-tasks tasklist view](./maton_google-tasks_tasklist_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-tasks tasklists

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-tasks tasklist list
$ maton google-tasks tasklist create --title 'Sprint 12'
$ maton google-tasks tasklist update MTYxNzM4 --title 'Sprint 13'
$ maton google-tasks tasklist clear MTYxNzM4
{% endraw %}{% endhighlight %}

### See also

* [maton google-tasks](./maton_google-tasks)
