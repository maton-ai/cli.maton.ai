---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github release download

```
maton github release download [<tag>] [flags]
```

Download all release assets, or filter with --pattern (one or more glob expressions matched against the asset name). With no <tag>, --latest fetches the most recent non-prerelease.

### Options


<dl class="flags">
	<dt>
		<code>--clobber</code></dt>
	<dd>Overwrite existing files at the destination</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-D</code>, 
		<code>--dir &lt;string&gt; (default &#34;.&#34;)</code></dt>
	<dd>Directory to write assets into</dd>

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
		<code>--latest</code></dt>
	<dd>Fetch the most recent non-prerelease release</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--pattern &lt;pattern&gt;</code></dt>
	<dd>Glob pattern(s) to match asset names</dd>

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
$ maton github release download v1.0.0 --repo maton-ai/cli
$ maton github release download v1.0.0 --repo maton-ai/cli --pattern '*.tar.gz' --dir dist/
$ maton github release download --repo maton-ai/cli --latest
{% endraw %}{% endhighlight %}

### See also

* [maton github release](./maton_github_release)
