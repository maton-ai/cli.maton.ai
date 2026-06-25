---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack user

List, get, and look up workspace users

### Available commands

* [maton slack user get](/manual/maton/slack/user/get)
* [maton slack user list](/manual/maton/slack/user/list)
* [maton slack user lookup](/manual/maton/slack/user/lookup)
* [maton slack user presence](/manual/maton/slack/user/presence)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack user list
$ maton slack user get U0123456789
$ maton slack user lookup --email alice@example.com
$ maton slack user presence U0123456789
{% endraw %}{% endhighlight %}

### See also

* [maton slack](/manual/maton/slack)
