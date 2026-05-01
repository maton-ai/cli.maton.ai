---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github repo create

```
maton github repo create <name> [flags]
```

Create a repository owned by the authenticated user, or by the org named via 'owner/name' as the positional argument. Defaults to a public repo with no template, license, or .gitignore.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-d</code>, 
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description of the repository</dd>

	<dt>
		<code>--disable-issues</code></dt>
	<dd>Disable issues for the new repo</dd>

	<dt>
		<code>--disable-wiki</code></dt>
	<dd>Disable wikis for the new repo</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--from-template &lt;owner/name&gt;</code></dt>
	<dd>Template repo to base this on, in owner/name form</dd>

	<dt><code>-g</code>, 
		<code>--gitignore &lt;string&gt;</code></dt>
	<dd>.gitignore template name (e.g. Go, Node)</dd>

	<dt><code>-h</code>, 
		<code>--homepage &lt;string&gt;</code></dt>
	<dd>Homepage URL</dd>

	<dt>
		<code>--include-all-branches</code></dt>
	<dd>(template only) include all branches, not just default</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-l</code>, 
		<code>--license &lt;string&gt;</code></dt>
	<dd>License keyword (e.g. mit, apache-2.0)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-t</code>, 
		<code>--team &lt;string&gt;</code></dt>
	<dd>(org only) team slug to grant access to the repo</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--visibility &lt;string&gt; (default &#34;public&#34;)</code></dt>
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
$ maton github repo create my-thing --description "A new project" --visibility private
$ maton github repo create maton-ai/my-org-thing --visibility public --license MIT
{% endraw %}{% endhighlight %}

### See also

* [maton github repo](/manual/maton/github/repo)
