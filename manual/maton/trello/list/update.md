---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello list update

```
maton trello list update <id> [flags]
```

Update list properties. To archive a list pass --closed; the list
is hidden from the board but can be unarchived in the Trello UI.


### Options


<dl class="flags">
	<dt><code>-b</code>, 
		<code>--board &lt;string&gt;</code></dt>
	<dd>Move the list to this board ID</dd>

	<dt>
		<code>--closed</code></dt>
	<dd>Archive (true) or unarchive (false) the list</dd>

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
		<code>--name &lt;string&gt;</code></dt>
	<dd>New list name</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--pos &lt;string&gt;</code></dt>
	<dd>Position: top, bottom, or a number</dd>

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
$ maton trello list update 5f1a... --name 'Renamed'
$ maton trello list update 5f1a... --pos top
$ maton trello list update 5f1a... --closed
$ maton trello list update 5f1a... --board 6b2c...
{% endraw %}{% endhighlight %}

### See also

* [maton trello list](/manual/maton/trello/list)
