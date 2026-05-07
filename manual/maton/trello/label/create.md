---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello label create

Create a new label on a board

```
maton trello label create [flags]
```

### Options


<dl class="flags">
	<dt><code>-b</code>, 
		<code>--board &lt;string&gt;</code></dt>
	<dd>Board ID to add the label to (required)</dd>

	<dt>
		<code>--color &lt;string&gt;</code></dt>
	<dd>Label color (yellow, purple, blue, red, green, orange, black, sky, pink, lime, null)</dd>

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
	<dd>Label name (required)</dd>

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
$ maton trello label create --board 5f1a... --name 'Bug' --color red
$ maton trello label create -b 5f1a... --name 'Untriaged'
{% endraw %}{% endhighlight %}

### See also

* [maton trello label](/manual/maton/trello/label)
