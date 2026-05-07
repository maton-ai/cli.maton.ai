---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello label list

List labels on a board

```
maton trello label list [flags]
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
$ maton trello label list --board 5f1a2b3c4d5e6f7a8b9c0d1e
$ maton trello label list -b 5f1a... --json
{% endraw %}{% endhighlight %}

### See also

* [maton trello label](/manual/maton/trello/label)
