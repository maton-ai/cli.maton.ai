---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira transition

List and apply workflow transitions

### Available commands

* [maton jira transition apply](/manual/maton/jira/transition/apply)
* [maton jira transition list](/manual/maton/jira/transition/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton jira transitions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton jira cloud list
$ maton jira transition list PROJ-123 --cloud-id <id>
$ maton jira transition apply PROJ-123 --cloud-id <id> --id 31
{% endraw %}{% endhighlight %}

### See also

* [maton jira](/manual/maton/jira)
