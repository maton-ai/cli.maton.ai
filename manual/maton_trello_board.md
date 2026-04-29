---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello board

Manage Trello boards (list, view, create)

### Available commands

* [maton trello board create](./maton_trello_board_create)
* [maton trello board list](./maton_trello_board_list)
* [maton trello board view](./maton_trello_board_view)


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
$ maton trello board create --name 'Launch' --desc 'Cross-team' --permission org
{% endraw %}{% endhighlight %}

### See also

* [maton trello](./maton_trello)
