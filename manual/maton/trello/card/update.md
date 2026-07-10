---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello card update

Update a card's properties

```
maton trello card update <id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--closed</code></dt>
	<dd>Archive (true) or unarchive (false) the card</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--desc &lt;string&gt;</code></dt>
	<dd>New description</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--due &lt;string&gt;</code></dt>
	<dd>New due date (ISO 8601)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-l</code>, 
		<code>--list &lt;string&gt;</code></dt>
	<dd>Move the card to this list ID</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>New card name</dd>

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
$ maton trello card update 5f1a... --name 'New title'
$ maton trello card update 5f1a... --list 6a2b...
$ maton trello card update 5f1a... --closed
{% endraw %}{% endhighlight %}

### See also

* [maton trello card](/manual/maton/trello/card)
