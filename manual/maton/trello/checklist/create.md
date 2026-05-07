---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello checklist create

Create a checklist on a card

```
maton trello checklist create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--card &lt;string&gt;</code></dt>
	<dd>Card ID to attach the checklist to (required)</dd>

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
	<dd>Checklist name (required)</dd>

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
$ maton trello checklist create --card 5f1a... --name 'Acceptance criteria'
$ maton trello checklist create --card 5f1a... --name 'Tasks' --pos top
{% endraw %}{% endhighlight %}

### See also

* [maton trello checklist](/manual/maton/trello/checklist)
