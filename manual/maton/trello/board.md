---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello board

Manage Trello boards (list, view, create, update, delete)

### Available commands

* [maton trello board create](/manual/maton/trello/board/create)
* [maton trello board delete](/manual/maton/trello/board/delete)
* [maton trello board list](/manual/maton/trello/board/list)
* [maton trello board update](/manual/maton/trello/board/update)
* [maton trello board view](/manual/maton/trello/board/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton trello boards

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trello board list
$ maton trello board view 5f1a2b3c4d5e6f7a8b9c0d1e
$ maton trello board create --name 'Q3 Roadmap'
$ maton trello board update 5f1a... --name 'Renamed'
$ maton trello board delete 5f1a...
{% endraw %}{% endhighlight %}

### See also

* [maton trello](/manual/maton/trello)
