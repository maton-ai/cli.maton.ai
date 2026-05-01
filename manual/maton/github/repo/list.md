---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github repo list

```
maton github repo list [<owner>] [flags]
```

Lists repositories. With no positional argument, lists the authenticated user's repositories (uses /user/repos and supports --visibility and --affiliation). With <owner>, lists that user's or org's repositories (auto-detects user vs org).

### Options


<dl class="flags">
	<dt>
		<code>--affiliation &lt;string&gt;</code></dt>
	<dd>(/user/repos only) comma-separated: owner, collaborator, organization_member</dd>

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

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 30)</code></dt>
	<dd>Maximum results per page (1-100)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--sort &lt;string&gt;</code></dt>
	<dd>Sort by: created, updated, pushed, full_name</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--type &lt;string&gt;</code></dt>
	<dd>Filter by repo type (all, owner, member, public, private, forks, sources)</dd>

	<dt>
		<code>--visibility &lt;string&gt;</code></dt>
	<dd>(/user/repos only) all, public, or private</dd>
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
$ maton github repo list
$ maton github repo list maton-ai --paginate
$ maton github repo list --visibility private --affiliation owner
{% endraw %}{% endhighlight %}

### See also

* [maton github repo](/manual/maton/github/repo)
