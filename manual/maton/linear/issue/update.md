---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear issue update

Update an issue's fields

```
maton linear issue update <id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Assignee user UUID</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-d</code>, 
		<code>--description &lt;string&gt;</code></dt>
	<dd>New description</dd>

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
		<code>--priority &lt;string&gt;</code></dt>
	<dd>Priority (0=None, 1=Urgent, 2=High, 3=Medium, 4=Low)</dd>

	<dt>
		<code>--state &lt;string&gt;</code></dt>
	<dd>Workflow state UUID</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-file &lt;file&gt;</code></dt>
	<dd>Read description from file (or `-` for stdin)</dd>

	<dt><code>-t</code>, 
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
$ maton linear issue update MTN-527 -t 'New title'
$ maton linear issue update MTN-527 --priority 2
$ maton linear issue update MTN-527 --state <state-uuid> --assignee <user-uuid>
{% endraw %}{% endhighlight %}

### See also

* [maton linear issue](/manual/maton/linear/issue)
