---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr merge

Merge a pull request

```
maton github pr merge <number-or-url> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--auto</code></dt>
	<dd>Enable auto-merge instead of merging immediately</dd>

	<dt><code>-m</code>, 
		<code>--commit-message &lt;string&gt;</code></dt>
	<dd>Body for the merge commit</dd>

	<dt><code>-t</code>, 
		<code>--commit-title &lt;string&gt;</code></dt>
	<dd>Title for the merge commit</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-d</code>, 
		<code>--delete-branch</code></dt>
	<dd>Delete the head branch after merge</dd>

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
		<code>--merge</code></dt>
	<dd>Use a merge commit (default)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--rebase</code></dt>
	<dd>Use rebase merging</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt>
		<code>--sha &lt;string&gt;</code></dt>
	<dd>Require this SHA to be at the head of the PR</dd>

	<dt>
		<code>--squash</code></dt>
	<dd>Use squash merging</dd>

	<dt>
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
$ maton github pr merge 123 --repo maton-ai/cli --squash --delete-branch
$ maton github pr merge 123 --repo maton-ai/cli --merge --commit-title "Merge: feature X"
$ maton github pr merge 123 --repo maton-ai/cli --auto --squash
{% endraw %}{% endhighlight %}

### See also

* [maton github pr](./maton_github_pr)
