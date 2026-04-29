---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue create

Create an issue

```
maton github issue create [flags]
```

### Options


<dl class="flags">
	<dt><code>-a</code>, 
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Comma-separated assignee logins (&#39;@me&#39; for self)</dd>

	<dt><code>-b</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Issue body (markdown)</dd>

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

	<dt><code>-l</code>, 
		<code>--label &lt;string&gt;</code></dt>
	<dd>Comma-separated label names</dd>

	<dt><code>-m</code>, 
		<code>--milestone &lt;string&gt;</code></dt>
	<dd>Milestone number</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;file&gt;</code></dt>
	<dd>Read body from file (or `-` for stdin)</dd>

	<dt><code>-t</code>, 
		<code>--title &lt;string&gt;</code></dt>
	<dd>Issue title (required)</dd>
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
$ maton github issue create --repo maton-ai/cli --title "Bug" --body "..."
$ maton github issue create --repo maton-ai/cli --title "Bug" --label bug --assignee @me
$ cat issue.md | maton github issue create --repo maton-ai/cli --title "Spec" -F -
{% endraw %}{% endhighlight %}

### See also

* [maton github issue](./maton_github_issue)
