---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr review

```
maton github pr review <number-or-url> [flags]
```

Submit an APPROVE / REQUEST_CHANGES / COMMENT review. Exactly one of --approve, --request-changes, or --comment must be set.

### Options


<dl class="flags">
	<dt><code>-a</code>, 
		<code>--approve</code></dt>
	<dd>Submit an APPROVE review</dd>

	<dt><code>-b</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Review body (markdown)</dd>

	<dt><code>-c</code>, 
		<code>--comment</code></dt>
	<dd>Submit a COMMENT review</dd>

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

	<dt><code>-r</code>, 
		<code>--request-changes</code></dt>
	<dd>Submit a REQUEST_CHANGES review</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-file &lt;file&gt;</code></dt>
	<dd>Read body from file (or `-` for stdin)</dd>
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
$ maton github pr review 123 --repo maton-ai/cli --approve
$ maton github pr review 123 --repo maton-ai/cli --request-changes --body "Tests please"
$ maton github pr review 123 --repo maton-ai/cli --comment --body "Looks promising"
{% endraw %}{% endhighlight %}

### See also

* [maton github pr](/manual/maton/github/pr)
