---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton yahoo-mail message

List, read, send, reply to, and organise messages

### Available commands

* [maton yahoo-mail message forward](/manual/maton/yahoo-mail/message/forward)
* [maton yahoo-mail message get](/manual/maton/yahoo-mail/message/get)
* [maton yahoo-mail message list](/manual/maton/yahoo-mail/message/list)
* [maton yahoo-mail message modify](/manual/maton/yahoo-mail/message/modify)
* [maton yahoo-mail message reply](/manual/maton/yahoo-mail/message/reply)
* [maton yahoo-mail message reply-all](/manual/maton/yahoo-mail/message/reply-all)
* [maton yahoo-mail message send](/manual/maton/yahoo-mail/message/send)
* [maton yahoo-mail message trash](/manual/maton/yahoo-mail/message/trash)
* [maton yahoo-mail message untrash](/manual/maton/yahoo-mail/message/untrash)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton yahoo-mail messages

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton yahoo-mail message list -L 5
$ maton yahoo-mail message get AASdfpO5xHnhSafuAprfE24JZdM --headers
$ maton yahoo-mail message send --to a@b.com --subject Hi --body 'Hello!'
$ maton yahoo-mail message reply AASdfpO5xHnhSafuAprfE24JZdM --body 'Got it'
{% endraw %}{% endhighlight %}

### See also

* [maton yahoo-mail](/manual/maton/yahoo-mail)
