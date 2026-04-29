---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana task create

```
maton asana task create [flags]
```

Create a task. Either --projects or --workspace is required; use --parent to create a subtask of an existing task. Workspace-scoped creation also requires --assignee (Asana API constraint).

### Options


<dl class="flags">
	<dt>
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Assignee gid (use &#39;me&#39; for yourself)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--due-on &lt;string&gt;</code></dt>
	<dd>Due date (YYYY-MM-DD)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>Task name (required)</dd>

	<dt>
		<code>--notes &lt;string&gt;</code></dt>
	<dd>Task description</dd>

	<dt>
		<code>--parent &lt;string&gt;</code></dt>
	<dd>Parent task gid (creates a subtask)</dd>

	<dt>
		<code>--projects &lt;string&gt;</code></dt>
	<dd>Comma-separated project gids</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-w</code>, 
		<code>--workspace &lt;string&gt;</code></dt>
	<dd>Workspace gid (one of --projects/--workspace/--parent; needs --assignee if alone)</dd>
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
$ maton asana task create --name 'Write spec' --projects 67890
$ maton asana task create --name 'Triage' --assignee me -w 12345
$ maton asana task create --name 'Subtask' --parent 11111
{% endraw %}{% endhighlight %}

### See also

* [maton asana task](./maton_asana_task)
