---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-tasks tasklist

List, get, create, update, and delete task lists

### Available commands

* [maton google-tasks tasklist clear](/manual/maton/google-tasks/tasklist/clear)
* [maton google-tasks tasklist create](/manual/maton/google-tasks/tasklist/create)
* [maton google-tasks tasklist delete](/manual/maton/google-tasks/tasklist/delete)
* [maton google-tasks tasklist get](/manual/maton/google-tasks/tasklist/get)
* [maton google-tasks tasklist list](/manual/maton/google-tasks/tasklist/list)
* [maton google-tasks tasklist update](/manual/maton/google-tasks/tasklist/update)


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

* [maton google-tasks](/manual/maton/google-tasks)
