---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack schedule list

List pending scheduled messages

```
maton slack schedule list [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Filter to a single channel ID</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--cursor &lt;string&gt;</code></dt>
	<dd>Pagination cursor from previous response</dd>

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
		<code>--latest &lt;string&gt;</code></dt>
	<dd>End of time range (Unix timestamp)</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 20)</code></dt>
	<dd>Max results per page</dd>

	<dt>
		<code>--oldest &lt;string&gt;</code></dt>
	<dd>Start of time range (Unix timestamp)</dd>

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
$ maton slack schedule list
$ maton slack schedule list --channel C0123456789
{% endraw %}{% endhighlight %}

### See also

* [maton slack schedule](/manual/maton/slack/schedule)
