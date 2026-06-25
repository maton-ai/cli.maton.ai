---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack message

Send, list, update, delete, and link messages

### Available commands

* [maton slack message delete](/manual/maton/slack/message/delete)
* [maton slack message list](/manual/maton/slack/message/list)
* [maton slack message permalink](/manual/maton/slack/message/permalink)
* [maton slack message replies](/manual/maton/slack/message/replies)
* [maton slack message reply](/manual/maton/slack/message/reply)
* [maton slack message send](/manual/maton/slack/message/send)
* [maton slack message update](/manual/maton/slack/message/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack message list --channel C0123456789
$ maton slack message send --channel C0123456789 --text 'Hello team'
$ maton slack message update --channel C012 --ts 1700000000.000100 --text 'Updated'
$ maton slack message delete --channel C012 --ts 1700000000.000100
{% endraw %}{% endhighlight %}

### See also

* [maton slack](/manual/maton/slack)
