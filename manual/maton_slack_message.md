---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack message

Send, list, update, delete, and link messages

### Available commands

* [maton slack message delete](./maton_slack_message_delete)
* [maton slack message list](./maton_slack_message_list)
* [maton slack message me](./maton_slack_message_me)
* [maton slack message permalink](./maton_slack_message_permalink)
* [maton slack message replies](./maton_slack_message_replies)
* [maton slack message reply](./maton_slack_message_reply)
* [maton slack message send](./maton_slack_message_send)
* [maton slack message update](./maton_slack_message_update)


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

* [maton slack](./maton_slack)
