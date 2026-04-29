---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira

Manage issues, projects, and comments in Jira.

### Available commands

* [maton jira cloud](./maton_jira_cloud)
* [maton jira comment](./maton_jira_comment)
* [maton jira issue](./maton_jira_issue)
* [maton jira project](./maton_jira_project)
* [maton jira transition](./maton_jira_transition)
* [maton jira whoami](./maton_jira_whoami)


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

* [maton](./maton)
