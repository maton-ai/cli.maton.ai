---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github release create

```
maton github release create <tag> [flags]
```

Create a release for an existing or new tag. The tag is created on
--target (defaults to the repository's default branch) if it does
not already exist on the remote.

Use --generate-notes to have GitHub auto-fill the release body from
the merged PRs since the previous tag.


### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--discussion-category &lt;string&gt;</code></dt>
	<dd>Start a release discussion in this category</dd>

	<dt>
		<code>--draft</code></dt>
	<dd>Save as a draft instead of publishing</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--generate-notes</code></dt>
	<dd>Auto-generate release notes from merged PRs since the previous tag</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--latest &lt;string&gt;</code></dt>
	<dd>Mark this release as the latest: &#39;true&#39;, &#39;false&#39;, or &#39;legacy&#39; (defaults to GitHub&#39;s auto-detection)</dd>

	<dt><code>-n</code>, 
		<code>--notes &lt;string&gt;</code></dt>
	<dd>Release notes (markdown)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--prerelease</code></dt>
	<dd>Mark the release as prerelease</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt>
		<code>--target &lt;string&gt;</code></dt>
	<dd>Target commitish (branch, tag, or sha; defaults to the repo&#39;s default branch)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;file&gt;</code></dt>
	<dd>Read notes from file (or `-` for stdin)</dd>

	<dt><code>-t</code>, 
		<code>--title &lt;string&gt;</code></dt>
	<dd>Release title (defaults to the tag name)</dd>
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
$ maton github release create v1.0.0 --repo maton-ai/cli --title "v1.0.0" --notes "First stable release"
$ maton github release create v1.1.0 --repo maton-ai/cli --generate-notes --draft
$ maton github release create v1.0.0-rc1 --repo maton-ai/cli --prerelease -F notes.md
{% endraw %}{% endhighlight %}

### See also

* [maton github release](./maton_github_release)
