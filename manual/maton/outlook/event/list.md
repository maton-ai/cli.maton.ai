---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook event list

List events from a calendar (default: primary calendar)

```
maton outlook event list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--calendar &lt;string&gt;</code></dt>
	<dd>Calendar ID (default: primary calendar)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--filter &lt;string&gt;</code></dt>
	<dd>OData $filter expression (e.g. &#34;start/dateTime ge &#39;2026-01-01&#39;&#34;)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--orderby &lt;string&gt;</code></dt>
	<dd>OData $orderby (e.g. start/dateTime)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--select &lt;string&gt;</code></dt>
	<dd>Comma-separated fields (e.g. subject,start,end)</dd>

	<dt>
		<code>--skip &lt;string&gt;</code></dt>
	<dd>Number of results to skip (pagination)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--top &lt;string&gt; (default &#34;10&#34;)</code></dt>
	<dd>OData $top — max results per page</dd>
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
$ maton outlook event list
$ maton outlook event list --calendar AQMk... --top 50
$ maton outlook event list --filter "start/dateTime ge '2026-05-01'" --orderby "start/dateTime"
$ maton outlook event list --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton outlook event](/manual/maton/outlook/event)
