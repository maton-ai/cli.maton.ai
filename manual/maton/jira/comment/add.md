---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira comment add

```
maton jira comment add <issue-key> [flags]
```

Post a plain-text comment on an issue. The body is automatically wrapped in Atlassian Document Format.

### Options


<dl class="flags">
	<dt>
		<code>--body &lt;string&gt;</code></dt>
	<dd>Comment text (one of --body/--text-from-file; wrapped in ADF)</dd>

	<dt>
		<code>--cloud-id &lt;string&gt;</code></dt>
	<dd>Jira Cloud ID (run &#39;maton jira cloud list&#39; to discover)</dd>

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

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;file&gt;</code></dt>
	<dd>Read body from file (or `-` for stdin; one of --body/--text-from-file)</dd>
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
$ maton jira comment add PROJ-123 --cloud-id abc-123 --body 'Looking into this now'
$ cat note.md | maton jira comment add PROJ-123 --cloud-id abc-123 -F -
{% endraw %}{% endhighlight %}

### See also

* [maton jira comment](/manual/maton/jira/comment)
