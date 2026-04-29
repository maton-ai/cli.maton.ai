---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello card create

Create a new card

```
maton trello card create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--desc &lt;string&gt;</code></dt>
	<dd>Card description</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--due &lt;string&gt;</code></dt>
	<dd>Due date (ISO 8601 format)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--label-ids &lt;string&gt;</code></dt>
	<dd>Comma-separated label IDs</dd>

	<dt><code>-l</code>, 
		<code>--list &lt;string&gt;</code></dt>
	<dd>ID of the list to add the card to (required)</dd>

	<dt>
		<code>--member-ids &lt;string&gt;</code></dt>
	<dd>Comma-separated member IDs</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>Card name (required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--pos &lt;string&gt; (default &#34;bottom&#34;)</code></dt>
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
$ maton trello card create --list 5f1a... --name 'Write spec'
$ maton trello card create -l 5f1a... --name 'Triage' --desc 'P1 bugs' --due 2026-12-01
{% endraw %}{% endhighlight %}

### See also

* [maton trello card](./maton_trello_card)
