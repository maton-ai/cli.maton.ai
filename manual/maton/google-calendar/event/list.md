---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar event list

List events on a calendar

```
maton google-calendar event list [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--calendar &lt;string&gt;</code></dt>
	<dd>Calendar ID (required, often &#34;primary&#34;)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Max events per page (1–2500)</dd>

	<dt>
		<code>--order-by &lt;string&gt;</code></dt>
	<dd>startTime|updated</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-Q</code>, 
		<code>--query &lt;string&gt;</code></dt>
	<dd>Free text search across event fields</dd>

	<dt>
		<code>--show-deleted</code></dt>
	<dd>Include deleted events</dd>

	<dt>
		<code>--single-events (default true)</code></dt>
	<dd>Expand recurring events into instances</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--time-max &lt;string&gt;</code></dt>
	<dd>Upper bound (RFC 3339)</dd>

	<dt>
		<code>--time-min &lt;string&gt;</code></dt>
	<dd>Lower bound (RFC 3339)</dd>

	<dt>
		<code>--timezone &lt;string&gt;</code></dt>
	<dd>IANA timezone for response times</dd>

	<dt>
		<code>--updated-min &lt;string&gt;</code></dt>
	<dd>Filter to events updated after this RFC 3339 timestamp</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton google-calendar events ls, maton google-calendar event ls

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-calendar event list -c primary
$ maton google-calendar event list -c primary --time-min 2026-06-17T00:00:00Z --time-max 2026-06-18T00:00:00Z
$ maton google-calendar event list -c primary --query 'standup' --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar event](/manual/maton/google-calendar/event)
