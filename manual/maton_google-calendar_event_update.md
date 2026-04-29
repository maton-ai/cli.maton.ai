---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar event update

```
maton google-calendar event update <event-id> [flags]
```

PATCH an event. Use the typed flags for common edits, or --body for arbitrary JSON. Only the fields supplied are changed; everything else is preserved server-side.

### Options


<dl class="flags">
	<dt>
		<code>--body &lt;string&gt;</code></dt>
	<dd>JSON object of fields to patch (escape hatch when typed flags don&#39;t cover it)</dd>

	<dt><code>-c</code>, 
		<code>--calendar &lt;string&gt;</code></dt>
	<dd>Calendar ID (required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>New event description/body</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--end &lt;string&gt;</code></dt>
	<dd>New end time, RFC 3339</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--location &lt;string&gt;</code></dt>
	<dd>New event location</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--send-updates &lt;string&gt;</code></dt>
	<dd>Notify attendees: all|externalOnly|none</dd>

	<dt>
		<code>--start &lt;string&gt;</code></dt>
	<dd>New start time, RFC 3339</dd>

	<dt>
		<code>--summary &lt;string&gt;</code></dt>
	<dd>New event summary/title</dd>

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
$ maton google-calendar event update evt-1 -c primary --summary 'New title'
$ maton google-calendar event update evt-1 -c primary --start 2026-06-17T10:00:00Z --end 2026-06-17T10:30:00Z
$ maton google-calendar event update evt-1 -c primary --body '{"colorId":"5"}'
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar event](./maton_google-calendar_event)
