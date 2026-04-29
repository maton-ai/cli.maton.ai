---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira issue

View, create, update, and search issues

### Available commands

* [maton jira issue create](./maton_jira_issue_create)
* [maton jira issue search](./maton_jira_issue_search)
* [maton jira issue update](./maton_jira_issue_update)
* [maton jira issue view](./maton_jira_issue_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton jira issues

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton jira cloud list
$ maton jira issue view PROJ-123 --cloud-id <id>
$ maton jira issue create --cloud-id <id> --project PROJ --summary 'Fix login'
$ maton jira issue search 'project = PROJ' --cloud-id <id>
{% endraw %}{% endhighlight %}

### See also

* [maton jira](./maton_jira)
