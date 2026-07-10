---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear issue list

List issues (optionally filtered by team and/or workflow state)

```
maton linear issue list [flags]
```

### Options


<dl class="flags">
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
		<code>--limit &lt;int&gt; (default 20)</code></dt>
	<dd>Max issues per page</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--state &lt;string&gt;</code></dt>
	<dd>Filter by workflow state type: triage, backlog, unstarted, started, completed, canceled</dd>

	<dt><code>-c</code>, 
		<code>--team &lt;string&gt;</code></dt>
	<dd>Filter by team key (e.g. MTN)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--title &lt;string&gt;</code></dt>
	<dd>Filter by title substring (case-insensitive)</dd>
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
$ maton linear issue list
$ maton linear issue list -L 10
$ maton linear issue list --team MTN
$ maton linear issue list -c MTN --state started
$ maton linear issue list --title 'login'
$ maton linear issue list --paginate --json
{% endraw %}{% endhighlight %}

### See also

* [maton linear issue](/manual/maton/linear/issue)
