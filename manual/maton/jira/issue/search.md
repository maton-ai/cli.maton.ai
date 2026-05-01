---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira issue search

```
maton jira issue search <jql> [flags]
```

Run a JQL query against the cloud and print the matching issues. Quote the JQL so the shell doesn't split it.

### Options


<dl class="flags">
	<dt>
		<code>--cloud-id &lt;string&gt;</code></dt>
	<dd>Jira Cloud ID (run &#39;maton jira cloud list&#39; to discover)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--fields &lt;string&gt;</code></dt>
	<dd>Comma-separated fields to return (e.g. summary,status,assignee)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 50)</code></dt>
	<dd>Maximum number of results per page</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton jira issue search 'project = PROJ AND status = "In Progress"' --cloud-id abc-123
$ maton jira issue search 'assignee = currentUser()' --cloud-id abc-123 --fields summary,status
$ maton jira issue search 'project = PROJ' --cloud-id abc-123 --paginate --format text
{% endraw %}{% endhighlight %}

### See also

* [maton jira issue](/manual/maton/jira/issue)
