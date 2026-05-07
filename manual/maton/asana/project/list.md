---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana project list

```
maton asana project list [flags]
```

List projects belonging to a workspace. Use 'maton asana workspace list' first to find the workspace gid.

### Options


<dl class="flags">
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
	<dd>Max results per page</dd>

	<dt>
		<code>--offset &lt;string&gt;</code></dt>
	<dd>Pagination offset token</dd>

	<dt>
		<code>--opt-fields &lt;string&gt;</code></dt>
	<dd>Comma-separated fields (e.g. name,owner,due_date)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

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
$ maton asana project list --workspace 12345
$ maton asana project list -w 12345 --opt-fields name,owner,due_date
$ maton asana project list -w 12345 --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton asana project](/manual/maton/asana/project)
