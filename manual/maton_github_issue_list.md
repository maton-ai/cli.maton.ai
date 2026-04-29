---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue list

```
maton github issue list [flags]
```

Pull requests are issues server-side, so they show up here too unless you filter by --label or --milestone in a way that excludes them. Use 'maton github pr list' to filter to PRs only.

### Options


<dl class="flags">
	<dt><code>-a</code>, 
		<code>--assignee &lt;string&gt;</code></dt>
	<dd>Filter by assignee login (or &#39;*&#39;/&#39;none&#39;)</dd>

	<dt><code>-A</code>, 
		<code>--author &lt;string&gt;</code></dt>
	<dd>Filter by issue author</dd>

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

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-l</code>, 
		<code>--label &lt;string&gt;</code></dt>
	<dd>Comma-separated label names to match</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 30)</code></dt>
	<dd>Maximum results per page (1-100)</dd>

	<dt>
		<code>--mention &lt;string&gt;</code></dt>
	<dd>Filter to issues mentioning a user</dd>

	<dt><code>-m</code>, 
		<code>--milestone &lt;string&gt;</code></dt>
	<dd>Filter by milestone (number or *)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt>
		<code>--sort &lt;string&gt;</code></dt>
	<dd>Sort by: created, updated, comments</dd>

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
$ maton github issue list --repo maton-ai/cli --state open
$ maton github issue list --repo maton-ai/cli --label "bug,good first issue"
$ maton github issue list --repo maton-ai/cli --paginate --format text
{% endraw %}{% endhighlight %}

### See also

* [maton github issue](./maton_github_issue)
