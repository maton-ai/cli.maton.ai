---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue comment

Add a comment to an issue

```
maton github issue comment <number-or-url> [flags]
```

### Options


<dl class="flags">
	<dt><code>-b</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Comment body (markdown) (required, or use --text-file)</dd>

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

	<dt><code>-F</code>, 
		<code>--text-file &lt;file&gt;</code></dt>
	<dd>Read body from file (or `-` for stdin) (required, or use --body)</dd>
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
$ maton github issue comment 123 --repo maton-ai/cli --body "Looking into this now"
$ cat note.md | maton github issue comment 123 --repo maton-ai/cli -F -
{% endraw %}{% endhighlight %}

### See also

* [maton github issue](/manual/maton/github/issue)
