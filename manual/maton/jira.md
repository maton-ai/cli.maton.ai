---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira

Manage issues, projects, and comments in Jira.

### Resource commands

* [maton jira cloud](/manual/maton/jira/cloud)
* [maton jira comment](/manual/maton/jira/comment)
* [maton jira issue](/manual/maton/jira/issue)
* [maton jira issuetype](/manual/maton/jira/issuetype)
* [maton jira priority](/manual/maton/jira/priority)
* [maton jira project](/manual/maton/jira/project)
* [maton jira status](/manual/maton/jira/status)
* [maton jira transition](/manual/maton/jira/transition)
* [maton jira user](/manual/maton/jira/user)


### Auth commands

* [maton jira whoami](/manual/maton/jira/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton jira cloud list
$ maton jira whoami --cloud-id abc-123
$ maton jira issue search 'project = PROJ AND status = "In Progress"' --cloud-id abc-123
$ maton jira issue create --cloud-id abc-123 --project PROJ --summary 'Fix login'
$ maton jira transition list PROJ-123 --cloud-id abc-123
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
