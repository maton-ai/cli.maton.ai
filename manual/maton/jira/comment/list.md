---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira comment list

```
maton jira comment list <issue-key> [flags]
```

List comments on an issue. Jira's comment endpoint paginates with startAt/maxResults rather than nextPageToken — re-run with --start-at to walk past the first page.

### Options


<dl class="flags">
	<dt>
		<code>--cloud-id &lt;string&gt;</code></dt>
	<dd>Jira Cloud ID, run &#39;maton jira cloud list&#39; to discover (required)</dd>

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

	<dt><code>-L</code>, 
		<code>--max-results &lt;int&gt; (default 50)</code></dt>
	<dd>Maximum number of comments to return</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--start-at &lt;int&gt; (default 0)</code></dt>
	<dd>Index of the first comment to return (for pagination)</dd>

	<dt><code>-t</code>, 
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
$ maton jira comment list PROJ-123 --cloud-id abc-123
$ maton jira comment list PROJ-123 --cloud-id abc-123 --max-results 100
$ maton jira comment list PROJ-123 --cloud-id abc-123 --start-at 50 --json
{% endraw %}{% endhighlight %}

### See also

* [maton jira comment](/manual/maton/jira/comment)
