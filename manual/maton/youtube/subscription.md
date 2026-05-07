---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube subscription

List, create, and delete channel subscriptions

### Available commands

* [maton youtube subscription create](/manual/maton/youtube/subscription/create)
* [maton youtube subscription delete](/manual/maton/youtube/subscription/delete)
* [maton youtube subscription list](/manual/maton/youtube/subscription/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton youtube sub,  maton youtube subs, maton youtube subscriptions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton youtube subscription list
$ maton youtube subscription list --for-channel UC1
$ maton youtube subscription create --channel UC1
$ maton youtube subscription delete <subscriptionId>
{% endraw %}{% endhighlight %}

### See also

* [maton youtube](/manual/maton/youtube)
