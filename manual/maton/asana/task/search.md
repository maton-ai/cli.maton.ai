---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana task search

```
maton asana task search [flags]
```

Search a workspace's tasks by text and/or filters. Requires an Asana Premium subscription. The endpoint does not use cursor pagination — pass --limit to cap results.

### Options


<dl class="flags">
	<dt>
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Comma-separated assignee gids (use &#39;me&#39; for yourself)</dd>

	<dt>
		<code>--completed</code></dt>
	<dd>Filter by completion status (use --completed=false for open tasks)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Max results to return</dd>

	<dt>
		<code>--opt-fields &lt;string&gt;</code></dt>
	<dd>Comma-separated fields to return</dd>

	<dt>
		<code>--projects &lt;string&gt;</code></dt>
	<dd>Comma-separated project gids</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--text &lt;string&gt;</code></dt>
	<dd>Text to search for</dd>

	<dt><code>-w</code>, 
		<code>--workspace &lt;string&gt;</code></dt>
	<dd>Workspace gid (required)</dd>
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
$ maton asana task search -w 12345 --text 'quarterly report'
$ maton asana task search -w 12345 --assignee me --completed=false
$ maton asana task search -w 12345 --projects 67890,67891 --text spec
{% endraw %}{% endhighlight %}

### See also

* [maton asana task](/manual/maton/asana/task)
