---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar freebusy query

Query busy intervals on one or more calendars

```
maton google-calendar freebusy query [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--calendar &lt;stringArray&gt;</code></dt>
	<dd>Calendar ID to query (repeatable, required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--time-max &lt;string&gt;</code></dt>
	<dd>Upper bound (RFC 3339, required)</dd>

	<dt>
		<code>--time-min &lt;string&gt;</code></dt>
	<dd>Lower bound (RFC 3339, required)</dd>

	<dt>
		<code>--timezone &lt;string&gt;</code></dt>
	<dd>IANA timezone for response times</dd>
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
$ maton google-calendar freebusy query --time-min 2026-06-17T00:00:00Z --time-max 2026-06-18T00:00:00Z --calendar primary
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar freebusy](/manual/maton/google-calendar/freebusy)
