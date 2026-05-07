---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trello checkitem update

```
maton trello checkitem update <item-id> [flags]
```

Trello's update endpoint lives under the parent card, so --card is
required. Pass --state complete or --state incomplete to toggle
the checkbox.


### Options


<dl class="flags">
	<dt>
		<code>--card &lt;string&gt;</code></dt>
	<dd>Card ID the item belongs to (required)</dd>

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
	<dd>New item text</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--pos &lt;string&gt;</code></dt>
	<dd>Position: top, bottom, or a number</dd>

	<dt>
		<code>--state &lt;string&gt;</code></dt>
	<dd>complete or incomplete</dd>

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
$ maton trello checkitem update ci-1 --card c-1 --name 'Renamed'
$ maton trello checkitem update ci-1 --card c-1 --state complete
{% endraw %}{% endhighlight %}

### See also

* [maton trello checkitem](/manual/maton/trello/checkitem)
