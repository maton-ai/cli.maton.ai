---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github release delete

Delete a release

```
maton github release delete <tag> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--cleanup-tag</code></dt>
	<dd>Also delete the underlying git tag</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--yes</code></dt>
	<dd>Confirm without prompting</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton github releases remove, maton github release remove

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github release delete v1.0.0 --repo maton-ai/cli --yes
$ maton github release delete v1.0.0 --repo maton-ai/cli --yes --cleanup-tag
{% endraw %}{% endhighlight %}

### See also

* [maton github release](/manual/maton/github/release)
