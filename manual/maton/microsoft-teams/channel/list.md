---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams channel list

List channels in a team

```
maton microsoft-teams channel list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--filter &lt;string&gt;</code></dt>
	<dd>OData $filter (e.g. &#34;membershipType eq &#39;private&#39;&#34;)</dd>

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
		<code>--select &lt;string&gt;</code></dt>
	<dd>Comma-separated fields to return</dd>

	<dt>
		<code>--team &lt;string&gt;</code></dt>
	<dd>Team ID (required)</dd>

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
$ maton microsoft-teams channel list --team 19:abc...
$ maton microsoft-teams channel list --team 19:abc... --filter "membershipType eq 'private'"
$ maton microsoft-teams channel list --team 19:abc... --json
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams channel](/manual/maton/microsoft-teams/channel)
