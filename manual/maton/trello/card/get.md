---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello card get

Get a card by ID

```
maton trello card get <id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--checklists &lt;string&gt; (default &#34;none&#34;)</code></dt>
	<dd>Include checklists: all, none</dd>

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
		<code>--members</code></dt>
	<dd>Include member details</dd>

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


### ALIASES

 maton trello cards view, maton trello card view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trello card get 5f1a2b3c4d5e6f7a8b9c0d1e
$ maton trello card get 5f1a... --members --checklists all
{% endraw %}{% endhighlight %}

### See also

* [maton trello card](/manual/maton/trello/card)
