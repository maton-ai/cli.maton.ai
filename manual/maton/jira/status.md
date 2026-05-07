---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira status

List statuses

### Available commands

* [maton jira status list](/manual/maton/jira/status/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton jira statuses

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton jira status list --cloud-id <id>
{% endraw %}{% endhighlight %}

### See also

* [maton jira](/manual/maton/jira)
