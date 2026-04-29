---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr edit

Edit a pull request

```
maton github pr edit <number-or-url> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--add-assignee &lt;string&gt;</code></dt>
	<dd>Comma-separated assignees to add</dd>

	<dt>
		<code>--add-label &lt;string&gt;</code></dt>
	<dd>Comma-separated labels to add</dd>

	<dt>
		<code>--add-reviewer &lt;string&gt;</code></dt>
	<dd>Comma-separated reviewers to request</dd>

	<dt><code>-B</code>, 
		<code>--base &lt;string&gt;</code></dt>
	<dd>Change the base branch</dd>

	<dt><code>-b</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>New body</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--remove-assignee &lt;string&gt;</code></dt>
	<dd>Comma-separated assignees to remove</dd>

	<dt>
		<code>--remove-label &lt;string&gt;</code></dt>
	<dd>Comma-separated labels to remove</dd>

	<dt>
		<code>--remove-reviewer &lt;string&gt;</code></dt>
	<dd>Comma-separated reviewers to remove</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt>
		<code>--state &lt;string&gt;</code></dt>
	<dd>open or closed</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;file&gt;</code></dt>
	<dd>Read body from file (or `-` for stdin)</dd>

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
$ maton github pr edit 123 --repo maton-ai/cli --title "New title"
$ maton github pr edit 123 --repo maton-ai/cli --add-reviewer alice --add-reviewer bob
{% endraw %}{% endhighlight %}

### See also

* [maton github pr](./maton_github_pr)
