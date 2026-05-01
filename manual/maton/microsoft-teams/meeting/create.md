---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton microsoft-teams meeting create

Create an online meeting

```
maton microsoft-teams meeting create [flags]
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
		<code>--end &lt;string&gt;</code></dt>
	<dd>End time, ISO 8601 (required)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--start &lt;string&gt;</code></dt>
	<dd>Start time, ISO 8601 (required)</dd>

	<dt>
		<code>--subject &lt;string&gt;</code></dt>
	<dd>Meeting subject (required)</dd>

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
$ maton microsoft-teams meeting create --subject 'Team Sync' \
    --start 2026-02-18T10:00:00Z --end 2026-02-18T11:00:00Z
{% endraw %}{% endhighlight %}

### See also

* [maton microsoft-teams meeting](/manual/maton/microsoft-teams/meeting)
