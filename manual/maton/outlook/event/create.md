---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook event create

Create a calendar event

```
maton outlook event create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--attendees &lt;string&gt;</code></dt>
	<dd>Attendee email(s), comma-separated</dd>

	<dt><code>-t</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Event body content</dd>

	<dt><code>-F</code>, 
		<code>--body-file &lt;string&gt;</code></dt>
	<dd>Read event body from a file path (or &#39;-&#39; for stdin)</dd>

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
		<code>--end &lt;string&gt;</code></dt>
	<dd>End time, ISO 8601 e.g. 2026-05-10T11:00:00 (required)</dd>

	<dt>
		<code>--html</code></dt>
	<dd>Treat body as HTML (default: plain text)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--location &lt;string&gt;</code></dt>
	<dd>Location display name</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--start &lt;string&gt;</code></dt>
	<dd>Start time, ISO 8601 e.g. 2026-05-10T10:00:00 (required)</dd>

	<dt>
		<code>--subject &lt;string&gt;</code></dt>
	<dd>Event subject (required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--timezone &lt;string&gt; (default &#34;UTC&#34;)</code></dt>
	<dd>IANA or Windows timezone name (default: UTC)</dd>
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
$ maton outlook event create --subject "Sync" --start 2026-05-10T10:00:00 --end 2026-05-10T11:00:00
$ maton outlook event create --subject Review --start 2026-05-10T14:00:00 --end 2026-05-10T15:00:00 --timezone "Pacific Standard Time" --attendees alice@example.com,bob@example.com --location "Room 4"
$ maton outlook event create --calendar AQMk... --subject 1:1 --start 2026-05-10T09:00:00 --end 2026-05-10T09:30:00 --body "Agenda..." --html
{% endraw %}{% endhighlight %}

### See also

* [maton outlook event](/manual/maton/outlook/event)
