---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack conversation open

Open a DM (or group DM with multiple users) — or resume an existing conversation

```
maton slack conversation open [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Resume an existing conversation by ID (one of --users/--channel)</dd>

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
		<code>--return-im</code></dt>
	<dd>Return the full IM channel object</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--users &lt;string&gt;</code></dt>
	<dd>Comma-separated user IDs to open a DM with (one of --users/--channel)</dd>
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
$ maton slack conversation open --users U0123456789
$ maton slack conversation open --users U0123456789,U9876543210
$ maton slack conversation open --channel D0123456789
{% endraw %}{% endhighlight %}

### See also

* [maton slack conversation](/manual/maton/slack/conversation)
