---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github label clone

```
maton github label clone <source-repo> [flags]
```

Copy each label (name, color, description) from <source-repo> into the repo named by --repo. With --force, an existing label of the same name on the destination is patched in place; without it, the destination's existing label wins (the create returns 422 and is treated as success).

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt><code>-f</code>, 
		<code>--force</code></dt>
	<dd>Patch existing labels on the destination instead of skipping</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

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
$ maton github label clone cli/cli --repo maton-ai/fork
$ maton github label clone cli/cli --repo maton-ai/fork --force
{% endraw %}{% endhighlight %}

### See also

* [maton github label](/manual/maton/github/label)
