---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-tasks task update

Update a task (partial update)

```
maton google-tasks task update <task-id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--due &lt;string&gt;</code></dt>
	<dd>New due date (YYYY-MM-DD or RFC 3339)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-l</code>, 
		<code>--list &lt;string&gt;</code></dt>
	<dd>Task list ID (required)</dd>

	<dt>
		<code>--notes &lt;string&gt;</code></dt>
	<dd>New notes/description</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--status &lt;string&gt;</code></dt>
	<dd>Status: needsAction or completed</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--title &lt;string&gt;</code></dt>
	<dd>New title</dd>
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
$ maton google-tasks task update OTQyNzc -l MTYxNzM4 --title 'New title'
$ maton google-tasks task update OTQyNzc -l MTYxNzM4 --status completed
$ maton google-tasks task update OTQyNzc -l MTYxNzM4 --due 2026-12-15
{% endraw %}{% endhighlight %}

### See also

* [maton google-tasks task](./maton_google-tasks_task)
