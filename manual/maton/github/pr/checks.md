---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr checks

```
maton github pr checks <number-or-url> [flags]
```

Lists check runs for the PR's head commit. By default, runs whose
conclusion is "skipped" are hidden so the real signal isn't drowned
out — pass --all to see everything. Hidden runs are reported in a
footer.

### Options


<dl class="flags">
	<dt>
		<code>--all</code></dt>
	<dd>Include skipped runs in the output</dd>

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
$ maton github pr checks 123 --repo maton-ai/cli
$ maton github pr checks 123 --repo maton-ai/cli --format text
$ maton github pr checks 123 --repo maton-ai/cli --all
$ maton github pr checks https://github.com/maton-ai/cli/pull/123
{% endraw %}{% endhighlight %}

### See also

* [maton github pr](/manual/maton/github/pr)
