---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce record list

```
maton salesforce record list [flags]
```

List records in one of two modes:

Time-window mode (default) — record IDs updated or deleted within a window.
Maps to GET /sobjects/{type}/updated or /sobjects/{type}/deleted. Requires
--type, --start, --end (ISO-8601/RFC3339). Window must be at most 30 days;
--start cannot be more than 30 days in the past for --changes=deleted.

Recent mode (--recent) — records recently viewed by the connected user.
Maps to GET /recent. Accepts --limit; ignores --type/--start/--end/--changes.


### Options


<dl class="flags">
	<dt>
		<code>--changes &lt;string&gt; (default &#34;updated&#34;)</code></dt>
	<dd>Time-window mode: which change set to return (&#34;updated&#34; or &#34;deleted&#34;)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--end &lt;string&gt;</code></dt>
	<dd>Window end (time-window mode, ISO-8601)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Recent mode: max results</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--recent</code></dt>
	<dd>List recently viewed records (GET /recent) instead of a time window</dd>

	<dt>
		<code>--start &lt;string&gt;</code></dt>
	<dd>Window start (time-window mode, ISO-8601)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--type &lt;string&gt;</code></dt>
	<dd>sObject type (time-window mode, e.g. Contact, Account)</dd>
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
$ maton salesforce record list --type Contact --start 2026-04-01T00:00:00Z --end 2026-05-01T00:00:00Z
$ maton salesforce record list --type Contact --start 2026-04-01T00:00:00Z --end 2026-05-01T00:00:00Z --changes deleted
$ maton salesforce record list --recent
$ maton salesforce record list --recent --limit 25
{% endraw %}{% endhighlight %}

### See also

* [maton salesforce record](/manual/maton/salesforce/record)
