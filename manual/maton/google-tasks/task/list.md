---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-tasks task list

List tasks in a task list

```
maton google-tasks task list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--completed-max &lt;string&gt;</code></dt>
	<dd>Filter: completion date &lt;= (YYYY-MM-DD or RFC 3339)</dd>

	<dt>
		<code>--completed-min &lt;string&gt;</code></dt>
	<dd>Filter: completion date &gt;= (YYYY-MM-DD or RFC 3339)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--due-max &lt;string&gt;</code></dt>
	<dd>Filter: due date &lt;= (YYYY-MM-DD or RFC 3339)</dd>

	<dt>
		<code>--due-min &lt;string&gt;</code></dt>
	<dd>Filter: due date &gt;= (YYYY-MM-DD or RFC 3339)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Max tasks per page (1–100)</dd>

	<dt><code>-l</code>, 
		<code>--list &lt;string&gt;</code></dt>
	<dd>Task list ID (required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--show-completed</code></dt>
	<dd>Include completed tasks</dd>

	<dt>
		<code>--show-deleted</code></dt>
	<dd>Include deleted tasks</dd>

	<dt>
		<code>--show-hidden</code></dt>
	<dd>Include hidden tasks</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--updated-min &lt;string&gt;</code></dt>
	<dd>Filter: updated &gt;= (YYYY-MM-DD or RFC 3339)</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton google-tasks tasks ls, maton google-tasks task ls

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-tasks task list -l MTYxNzM4
$ maton google-tasks task list -l MTYxNzM4 --show-completed --paginate
$ maton google-tasks task list -l MTYxNzM4 --due-min 2026-01-01 --due-max 2026-12-31
{% endraw %}{% endhighlight %}

### See also

* [maton google-tasks task](/manual/maton/google-tasks/task)
