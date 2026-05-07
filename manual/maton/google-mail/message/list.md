---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail message list

```
maton google-mail message list [flags]
```

List messages in the active Gmail mailbox. Read-only — never modifies anything. Defaults to the unread queue (q=is:unread). Pass --hydrate to fetch From/Subject/Date for each result and render a table; without --hydrate the raw {messages: [{id, threadId}], ...} envelope is printed.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--hydrate</code></dt>
	<dd>Fetch From/Subject/Date for each result and render a table</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--label &lt;strings&gt;</code></dt>
	<dd>Restrict to label IDs (repeatable)</dd>

	<dt><code>-L</code>, 
		<code>--max &lt;int&gt; (default 20)</code></dt>
	<dd>Maximum messages per page</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--query &lt;string&gt; (default &#34;is:unread&#34;)</code></dt>
	<dd>Gmail search query</dd>

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
$ maton google-mail message list
$ maton google-mail message list -L 5 --query 'from:boss'
$ maton google-mail message list --hydrate --json
$ maton google-mail message list --paginate --query 'newer_than:7d'
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail message](/manual/maton/google-mail/message)
