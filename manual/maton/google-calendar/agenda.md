---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar agenda

```
maton google-calendar agenda [flags]
```

Read-only listing of events from one or all of your Google Calendars. Defaults to the next 1 day window. --today / --tomorrow snap to the user's Google account timezone; --timezone overrides.

### Options


<dl class="flags">
	<dt>
		<code>--calendar &lt;string&gt;</code></dt>
	<dd>Filter to a specific calendar name or ID</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--days &lt;int&gt; (default 0)</code></dt>
	<dd>Number of days ahead to show</dd>

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

	<dt>
		<code>--timezone &lt;string&gt;</code></dt>
	<dd>IANA timezone (default: Google account timezone)</dd>

	<dt>
		<code>--today</code></dt>
	<dd>Show today&#39;s events (account-day boundaries)</dd>

	<dt>
		<code>--tomorrow</code></dt>
	<dd>Show tomorrow&#39;s events</dd>

	<dt>
		<code>--week</code></dt>
	<dd>Show the next 7 days of events</dd>
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
$ maton google-calendar agenda
$ maton google-calendar agenda --today
$ maton google-calendar agenda --week
$ maton google-calendar agenda --days 3 --timezone America/New_York
$ maton google-calendar agenda --calendar 'Work' --format json
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar](/manual/maton/google-calendar)
