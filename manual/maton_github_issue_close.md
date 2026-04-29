---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue close

Close an issue

```
maton github issue close <number-or-url> [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--comment &lt;string&gt;</code></dt>
	<dd>Add a closing comment</dd>

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
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-r</code>, 
		<code>--reason &lt;string&gt;</code></dt>
	<dd>Close reason: completed or &#39;not planned&#39;</dd>

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
$ maton github issue close 123 --repo maton-ai/cli
$ maton github issue close 123 --repo maton-ai/cli --reason "not planned" --comment "tracked in #456"
$ maton github issue close https://github.com/maton-ai/cli/issues/123
{% endraw %}{% endhighlight %}

### See also

* [maton github issue](./maton_github_issue)
