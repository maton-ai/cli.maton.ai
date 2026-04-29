---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack conversation

List your conversations and open DMs

### Available commands

* [maton slack conversation list](./maton_slack_conversation_list)
* [maton slack conversation open](./maton_slack_conversation_open)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack conversation list
$ maton slack conversation list --types im,mpim
$ maton slack conversation open --users U0123456789
$ maton slack conversation open --channel D0123456789
{% endraw %}{% endhighlight %}

### See also

* [maton slack](./maton_slack)
