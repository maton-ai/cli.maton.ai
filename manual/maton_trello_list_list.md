---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello list list

List all lists on a board

```
maton trello list list [flags]
```

### Options


<dl class="flags">
	<dt><code>-b</code>, 
		<code>--board &lt;string&gt;</code></dt>
	<dd>Board ID (required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--filter &lt;string&gt; (default &#34;open&#34;)</code></dt>
	<dd>Filter: open, closed, all</dd>

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
$ maton trello list list --board 5f1a2b3c4d5e6f7a8b9c0d1e
$ maton trello list list -b 5f1a... --filter all
$ maton trello list list -b 5f1a... --format text
{% endraw %}{% endhighlight %}

### See also

* [maton trello list](./maton_trello_list)
