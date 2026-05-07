---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana task list

```
maton asana task list [flags]
```

Asana requires a scope: --project, --assignee plus --workspace, or --parent (lists subtasks of the given task). Use --incomplete to fetch only open tasks.

### Options


<dl class="flags">
	<dt>
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Assignee gid (use &#39;me&#39; for yourself)</dd>

	<dt>
		<code>--completed-since &lt;string&gt;</code></dt>
	<dd>Only tasks completed after this ISO timestamp</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--incomplete</code></dt>
	<dd>Only return open (incomplete) tasks</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Max results per page</dd>

	<dt>
		<code>--offset &lt;string&gt;</code></dt>
	<dd>Pagination offset token</dd>

	<dt>
		<code>--opt-fields &lt;string&gt;</code></dt>
	<dd>Comma-separated fields (e.g. name,completed,due_on,assignee)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent &lt;string&gt;</code></dt>
	<dd>Parent task gid (lists its subtasks)</dd>

	<dt>
		<code>--project &lt;string&gt;</code></dt>
	<dd>Project gid to list tasks from</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-w</code>, 
		<code>--workspace &lt;string&gt;</code></dt>
	<dd>Workspace gid (required when using --assignee)</dd>
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
$ maton asana task list --project 67890
$ maton asana task list --assignee me --workspace 12345
$ maton asana task list --assignee me -w 12345 --incomplete
$ maton asana task list --parent 11111
$ maton asana task list --project 67890 --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton asana task](/manual/maton/asana/task)
