---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github release upload

```
maton github release upload <tag> <file>... [flags]
```

Upload one or more files as release assets. Use --asset-name to override the asset name when uploading exactly one file (otherwise the basename is used). With --clobber, an existing asset of the same name is removed before re-uploading.

### Options


<dl class="flags">
	<dt>
		<code>--asset-name &lt;string&gt;</code></dt>
	<dd>Override the asset name (single-file uploads only)</dd>

	<dt>
		<code>--clobber</code></dt>
	<dd>Replace existing assets of the same name</dd>

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

	<dt>
		<code>--label &lt;string&gt;</code></dt>
	<dd>Asset label (display only)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

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
$ maton github release upload v1.0.0 ./dist/maton-darwin --repo maton-ai/cli
$ maton github release upload v1.0.0 ./dist/* --repo maton-ai/cli --clobber
{% endraw %}{% endhighlight %}

### See also

* [maton github release](./maton_github_release)
