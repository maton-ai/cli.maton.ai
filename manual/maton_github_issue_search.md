---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue search

```
maton github issue search [<query>...] [flags]
```

Searches /search/issues with q=is:issue. Positional args become free-text
keywords; flags map to qualifiers (author:, assignee:, repo:, etc.).
Pass '@me' to --author or --assignee for the authenticated user.

Unlike 'issue list', this hits the search index instead of a single
repo's issue stream, so --repo is optional. Without --repo or --owner
the search runs across all of GitHub.

### Options


<dl class="flags">
	<dt><code>-a</code>, 
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Filter by assignee (&#39;@me&#39; for self)</dd>

	<dt><code>-A</code>, 
		<code>--author &lt;string&gt;</code></dt>
	<dd>Filter by author (&#39;@me&#39; for self)</dd>

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
	<dd>Comma-separated label names to match</dd>

	<dt>
		<code>--language &lt;string&gt;</code></dt>
	<dd>Filter on coding language</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 30)</code></dt>
	<dd>Maximum results per page (1-100)</dd>

	<dt>
		<code>--order &lt;string&gt;</code></dt>
	<dd>Sort direction: asc or desc (only with --sort)</dd>

	<dt>
		<code>--owner &lt;string&gt;</code></dt>
	<dd>Filter on repository owner (user or org)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Restrict to a single repository in owner/repo form</dd>

	<dt>
		<code>--sort &lt;string&gt;</code></dt>
	<dd>Sort by: comments, reactions, interactions, created, updated</dd>

	<dt><code>-s</code>, 
		<code>--state &lt;string&gt;</code></dt>
	<dd>Filter by state: open or closed</dd>

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
$ maton github issue search "memory leak" --repo maton-ai/cli
$ maton github issue search --owner maton-ai --state open --label bug
$ maton github issue search --assignee @me --state open
$ maton github issue search "good first issue" --language go
{% endraw %}{% endhighlight %}

### See also

* [maton github issue](./maton_github_issue)
