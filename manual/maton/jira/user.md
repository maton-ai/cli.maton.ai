---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira user

Search users

### Available commands

* [maton jira user search](/manual/maton/jira/user/search)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton jira users

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton jira user search alice --cloud-id <id>
$ maton jira user search alice@example.com --cloud-id <id> --json
{% endraw %}{% endhighlight %}

### See also

* [maton jira](/manual/maton/jira)
