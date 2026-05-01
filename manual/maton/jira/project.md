---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira project

List projects

### Available commands

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
$ maton jira project list --cloud-id <id> --format text
{% endraw %}{% endhighlight %}

### See also

* [maton jira](/manual/maton/jira)
