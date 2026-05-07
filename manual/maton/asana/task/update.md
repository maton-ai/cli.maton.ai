---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana task update

```
maton asana task update <task-gid> [flags]
```

Modify one or more fields on an existing task. Use --clear-due to remove a previously-set due date.

### Options


<dl class="flags">
	<dt>
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Assignee gid (use &#39;me&#39; for yourself)</dd>

	<dt>
		<code>--clear-due</code></dt>
	<dd>Clear the due date</dd>

	<dt>
		<code>--completed</code></dt>
	<dd>Mark completed (use --completed=false to reopen)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--due-on &lt;string&gt;</code></dt>
	<dd>Due date (YYYY-MM-DD)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>New task name</dd>

	<dt>
		<code>--notes &lt;string&gt;</code></dt>
	<dd>Task description</dd>

	<dt><code>-t</code>, 
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
$ maton asana task update 11111 --completed true
$ maton asana task update 11111 --name 'New title' --due-on 2026-12-01
$ maton asana task update 11111 --clear-due
{% endraw %}{% endhighlight %}

### See also

* [maton asana task](/manual/maton/asana/task)
