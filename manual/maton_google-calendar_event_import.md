---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar event import

```
maton google-calendar event import [flags]
```

Used to copy an event from another calendar without losing its iCalUID/organizer. --body is the full event JSON; iCalUID is required by the API.

### Options


<dl class="flags">
	<dt>
		<code>--body &lt;string&gt;</code></dt>
	<dd>Full event JSON (required)</dd>

	<dt><code>-c</code>, 
		<code>--calendar &lt;string&gt;</code></dt>
	<dd>Calendar ID (required)</dd>

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

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

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
$ maton google-calendar event import -c primary --body '{"iCalUID":"abc@example.com","summary":"Imported","start":{"dateTime":"2026-06-17T09:00:00Z"},"end":{"dateTime":"2026-06-17T09:30:00Z"}}'
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar event](./maton_google-calendar_event)
