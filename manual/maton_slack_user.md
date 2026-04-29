---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack user

List, view, and look up workspace users

### Available commands

* [maton slack user list](./maton_slack_user_list)
* [maton slack user lookup](./maton_slack_user_lookup)
* [maton slack user presence](./maton_slack_user_presence)
* [maton slack user set-presence](./maton_slack_user_set-presence)
* [maton slack user view](./maton_slack_user_view)


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
$ maton slack user view U0123456789
$ maton slack user lookup --email alice@example.com
$ maton slack user presence U0123456789
{% endraw %}{% endhighlight %}

### See also

* [maton slack](./maton_slack)
