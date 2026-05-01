---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr create

```
maton github pr create [flags]
```

Open a PR against --base from --head. Both branches must already exist
on the remote. To open a cross-fork PR, use 'owner:branch' as --head.

Reviewers, assignees, and labels are applied as follow-up calls after
the PR is created (the create endpoint itself doesn't accept them).
Pass '@me' as a reviewer or assignee to mean the authenticated user.

### Options


<dl class="flags">
	<dt><code>-a</code>, 
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Comma-separated assignee logins (&#39;@me&#39; for self)</dd>

	<dt><code>-B</code>, 
		<code>--base &lt;string&gt;</code></dt>
	<dd>Target branch (required)</dd>

	<dt><code>-b</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>PR body (markdown)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-d</code>, 
		<code>--draft</code></dt>
	<dd>Open as a draft PR</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-H</code>, 
		<code>--head &lt;user:branch&gt;</code></dt>
	<dd>Source branch (user:branch or `branch`) (required)</dd>

	<dt>
		<code>--issue &lt;string&gt;</code></dt>
	<dd>Convert an existing issue number to a PR (instead of --title)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-l</code>, 
		<code>--label &lt;string&gt;</code></dt>
	<dd>Comma-separated label names to apply</dd>

	<dt>
		<code>--maintainer-can-modify (default true)</code></dt>
	<dd>Allow maintainers of the upstream to push to the PR</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt><code>-r</code>, 
		<code>--reviewer &lt;team:slug&gt;</code></dt>
	<dd>Comma-separated reviewer logins (or team:slug for teams; &#39;@me&#39; for self)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;file&gt;</code></dt>
	<dd>Read body from file (or `-` for stdin)</dd>

	<dt><code>-t</code>, 
		<code>--title &lt;string&gt;</code></dt>
	<dd>PR title</dd>
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
$ maton github pr create --repo maton-ai/cli --base main --head feature --title "New thing" --body "..."
$ maton github pr create --repo maton-ai/cli --base main --head feature --title "WIP" --reviewer alice,bob --label needs-review
$ maton github pr create --repo maton-ai/cli --base main --head fork-owner:branch --title "From fork" --draft
{% endraw %}{% endhighlight %}

### See also

* [maton github pr](/manual/maton/github/pr)
