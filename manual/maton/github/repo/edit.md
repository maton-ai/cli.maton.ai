---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github repo edit

```
maton github repo edit [flags]
```

Patch repository settings. Pass --topics with a comma-separated list to replace the topic set; an empty value clears them. Boolean flags only apply when explicitly set.

### Options


<dl class="flags">
	<dt>
		<code>--allow-auto-merge</code></dt>
	<dd>Allow auto-merge on PRs</dd>

	<dt>
		<code>--allow-merge (default true)</code></dt>
	<dd>Allow merge commits on PRs</dd>

	<dt>
		<code>--allow-rebase (default true)</code></dt>
	<dd>Allow rebase-merging on PRs</dd>

	<dt>
		<code>--allow-squash (default true)</code></dt>
	<dd>Allow squash-merging on PRs</dd>

	<dt>
		<code>--archived</code></dt>
	<dd>Archive (true) or unarchive (false) the repository</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--default-branch &lt;string&gt;</code></dt>
	<dd>New default branch name</dd>

	<dt>
		<code>--delete-branch-on-merge</code></dt>
	<dd>Delete head branches automatically after PR merge</dd>

	<dt><code>-d</code>, 
		<code>--description &lt;string&gt;</code></dt>
	<dd>New description</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--enable-issues (default true)</code></dt>
	<dd>Enable issues</dd>

	<dt>
		<code>--enable-projects (default true)</code></dt>
	<dd>Enable projects</dd>

	<dt>
		<code>--enable-wiki (default true)</code></dt>
	<dd>Enable wiki</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-h</code>, 
		<code>--homepage &lt;string&gt;</code></dt>
	<dd>New homepage URL</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--topics &lt;string&gt;</code></dt>
	<dd>Comma-separated topics to replace the set with (empty clears)</dd>

	<dt>
		<code>--visibility &lt;string&gt;</code></dt>
	<dd>public, private, or internal</dd>
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
$ maton github repo edit --repo maton-ai/cli --description "Maton CLI"
$ maton github repo edit --repo maton-ai/cli --topics cli,maton --enable-wiki=false
$ maton github repo edit --repo maton-ai/cli --visibility private
{% endraw %}{% endhighlight %}

### See also

* [maton github repo](/manual/maton/github/repo)
