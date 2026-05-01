---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello list create

Create a new list on a board

```
maton trello list create [flags]
```

### Options


<dl class="flags">
	<dt><code>-b</code>, 
		<code>--board &lt;string&gt;</code></dt>
	<dd>Board ID to add the list to (required)</dd>

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
		<code>--name &lt;string&gt;</code></dt>
	<dd>List name (required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--pos &lt;string&gt; (default &#34;top&#34;)</code></dt>
	<dd>Position: top, bottom, or a number</dd>

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
$ maton trello list create --board 5f1a... --name 'In Progress'
$ maton trello list create -b 5f1a... --name 'Done' --pos bottom
{% endraw %}{% endhighlight %}

### See also

* [maton trello list](/manual/maton/trello/list)
