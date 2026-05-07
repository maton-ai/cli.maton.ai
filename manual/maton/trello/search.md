---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello search

```
maton trello search [flags]
```

Wraps Trello's GET /search. By default Trello looks across the
authenticated member's accessible content; pass --boards to scope
to specific board IDs.


### Options


<dl class="flags">
	<dt>
		<code>--boards &lt;string&gt;</code></dt>
	<dd>Comma-separated board IDs to scope the search to (default &#39;mine&#39;)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Result limit applied to cards and boards (max 1000)</dd>

	<dt>
		<code>--models &lt;string&gt;</code></dt>
	<dd>Comma-separated model types: actions, boards, cards, members, organizations (default all)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--partial</code></dt>
	<dd>Match partial words</dd>

	<dt><code>-q</code>, 
		<code>--query &lt;string&gt;</code></dt>
	<dd>Search query (required, 1–16384 chars)</dd>

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
$ maton trello search --query 'release notes'
$ maton trello search --query 'bug' --models cards --limit 50
$ maton trello search --query 'planning' --boards b-1,b-2 --partial
{% endraw %}{% endhighlight %}

### See also

* [maton trello](/manual/maton/trello)
