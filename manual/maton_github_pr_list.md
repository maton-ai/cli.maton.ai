---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr list

```
maton github pr list [flags]
```

Lists PRs via /repos/{owner}/{repo}/pulls. When --label, --author, or
--assignee is set the request is routed through GitHub's search API
(/search/issues with q=is:pr+repo:owner/repo+...) since the REST
pulls endpoint cannot filter on those fields. Pass '@me' to --author
or --assignee for "the authenticated user".

### Options


<dl class="flags">
	<dt><code>-a</code>, 
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Filter by assignee (uses search API; &#39;@me&#39; for self)</dd>

	<dt><code>-A</code>, 
		<code>--author &lt;string&gt;</code></dt>
	<dd>Filter by PR author (uses search API; &#39;@me&#39; for self)</dd>

	<dt><code>-B</code>, 
		<code>--base &lt;string&gt;</code></dt>
	<dd>Filter by base branch</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--direction &lt;string&gt;</code></dt>
	<dd>Sort direction: asc or desc</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-H</code>, 
		<code>--head &lt;user:branch&gt;</code></dt>
	<dd>Filter by head ref (user:branch or `branch`)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-l</code>, 
		<code>--label &lt;string&gt;</code></dt>
	<dd>Comma-separated label names (uses search API)</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 30)</code></dt>
	<dd>Maximum results per page (1-100)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt>
		<code>--sort &lt;string&gt;</code></dt>
	<dd>Sort by: created, updated, popularity, long-running</dd>

	<dt><code>-s</code>, 
		<code>--state &lt;string&gt; (default &#34;open&#34;)</code></dt>
	<dd>Filter by state: open, closed, all</dd>

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
$ maton github pr list --repo maton-ai/cli --state open
$ maton github pr list --repo maton-ai/cli --base main --head feature
$ maton github pr list --repo maton-ai/cli --label bug --author @me
$ maton github pr list --repo maton-ai/cli --paginate --format text
{% endraw %}{% endhighlight %}

### See also

* [maton github pr](./maton_github_pr)
