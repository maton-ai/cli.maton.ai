---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira issue create

```
maton jira issue create [flags]
```

Create an issue with a project key, summary, and optional description. The description is automatically wrapped in Atlassian Document Format.

### Options


<dl class="flags">
	<dt>
		<code>--cloud-id &lt;string&gt;</code></dt>
	<dd>Jira Cloud ID (run &#39;maton jira cloud list&#39; to discover)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Issue description (wrapped in ADF)</dd>

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
		<code>--project &lt;string&gt;</code></dt>
	<dd>Project key, e.g. PROJ (required)</dd>

	<dt>
		<code>--summary &lt;string&gt;</code></dt>
	<dd>Issue summary/title (required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;file&gt;</code></dt>
	<dd>Read description from file (or `-` for stdin)</dd>

	<dt>
		<code>--type &lt;string&gt; (default &#34;Task&#34;)</code></dt>
	<dd>Issue type (e.g. Task, Bug, Story)</dd>
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
$ maton jira issue create --cloud-id abc-123 --project PROJ --summary 'Fix login'
$ maton jira issue create --cloud-id abc-123 --project PROJ --summary 'New bug' --type Bug --description 'Repro steps...'
$ cat description.md | maton jira issue create --cloud-id abc-123 --project PROJ --summary 'Spec' -F -
{% endraw %}{% endhighlight %}

### See also

* [maton jira issue](./maton_jira_issue)
