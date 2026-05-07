---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira issue update

Update an issue's fields

```
maton jira issue update <issue-key> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Account ID of the new assignee (use --unassign to clear)</dd>

	<dt>
		<code>--cloud-id &lt;string&gt;</code></dt>
	<dd>Jira Cloud ID, run &#39;maton jira cloud list&#39; to discover (required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>New description (wrapped in ADF)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--summary &lt;string&gt;</code></dt>
	<dd>New summary/title (at least one of --summary/--description/--text-file/--assignee/--unassign)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-file &lt;file&gt;</code></dt>
	<dd>Read description from file (or `-` for stdin)</dd>

	<dt>
		<code>--unassign</code></dt>
	<dd>Clear the assignee field</dd>
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
$ maton jira issue update PROJ-123 --cloud-id abc-123 --summary 'New title'
$ maton jira issue update PROJ-123 --cloud-id abc-123 --description 'Updated context'
$ maton jira issue update PROJ-123 --cloud-id abc-123 --assignee 5b10ac8d82e05b22cc7d4ef5
$ maton jira issue update PROJ-123 --cloud-id abc-123 --unassign
{% endraw %}{% endhighlight %}

### See also

* [maton jira issue](/manual/maton/jira/issue)
