---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar event create

```
maton google-calendar event create [flags]
```

Create a single event on a calendar (defaults to "primary"). Use --meet to attach a Google Meet conference link; the underlying conferenceData.createRequest is given a deterministic request ID derived from the event payload, so re-running the same command won't create duplicate Meet rooms.

### Options


<dl class="flags">
	<dt>
		<code>--attendee &lt;stringArray&gt;</code></dt>
	<dd>Attendee email (repeatable)</dd>

	<dt><code>-c</code>, 
		<code>--calendar &lt;string&gt; (default &#34;primary&#34;)</code></dt>
	<dd>Calendar ID</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Event description/body</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--end &lt;string&gt;</code></dt>
	<dd>End time, RFC 3339 (required)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--location &lt;string&gt;</code></dt>
	<dd>Event location</dd>

	<dt>
		<code>--meet</code></dt>
	<dd>Attach a Google Meet conference link</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--send-updates &lt;string&gt;</code></dt>
	<dd>Notify attendees: all|externalOnly|none</dd>

	<dt>
		<code>--start &lt;string&gt;</code></dt>
	<dd>Start time, RFC 3339 (required), e.g. 2026-06-17T09:00:00-07:00</dd>

	<dt>
		<code>--summary &lt;string&gt;</code></dt>
	<dd>Event summary/title (required)</dd>

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


### ALIASES

 maton google-calendar events insert, maton google-calendar event insert

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-calendar event create --summary 'Standup' --start 2026-06-17T09:00:00Z --end 2026-06-17T09:30:00Z
$ maton google-calendar event create --summary 'Review' --start ... --end ... --attendee alice@example.com --attendee bob@example.com
$ maton google-calendar event create --summary 'Demo' --start ... --end ... --meet
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar event](./maton_google-calendar_event)
