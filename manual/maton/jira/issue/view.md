---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira issue view

Get an issue by key (e.g. PROJ-123)

```
maton jira issue view <issue-key> [flags]
```

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

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

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
$ maton jira issue view PROJ-123 --cloud-id abc-123
{% endraw %}{% endhighlight %}

### See also

* [maton jira issue](/manual/maton/jira/issue)
