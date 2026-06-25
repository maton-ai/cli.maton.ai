---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams message get

Show a single message

```
maton microsoft-teams message get <message-id> [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Channel ID (with --team)</dd>

	<dt>
		<code>--chat &lt;string&gt;</code></dt>
	<dd>Chat ID (mutually exclusive with --team/--channel)</dd>

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

	<dt>
		<code>--team &lt;string&gt;</code></dt>
	<dd>Team ID (with --channel)</dd>

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

 maton microsoft-teams messages view, maton microsoft-teams message view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton microsoft-teams message get 1700000000000 --team 19:t... --channel 19:c...
$ maton microsoft-teams message get 1700000000000 --chat 19:abc...
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams message](/manual/maton/microsoft-teams/message)
