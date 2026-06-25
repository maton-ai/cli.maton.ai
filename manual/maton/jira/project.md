---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira project

Get and list projects

### Available commands

* [maton jira project get](/manual/maton/jira/project/get)
* [maton jira project list](/manual/maton/jira/project/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton jira projects

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton jira cloud list
$ maton jira project list --cloud-id <id>
$ maton jira project get PROJ --cloud-id <id>
{% endraw %}{% endhighlight %}

### See also

* [maton jira](/manual/maton/jira)
