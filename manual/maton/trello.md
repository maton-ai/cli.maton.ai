---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello

Manage boards, lists, and cards in Trello.

### Available commands

* [maton trello board](/manual/maton/trello/board)
* [maton trello card](/manual/maton/trello/card)
* [maton trello list](/manual/maton/trello/list)
* [maton trello member](/manual/maton/trello/member)
* [maton trello whoami](/manual/maton/trello/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trello whoami
$ maton trello board list
$ maton trello list list --board 5f1a2b3c4d5e6f7a8b9c0d1e
$ maton trello card create --list 5f1a... --name 'Write spec'
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
