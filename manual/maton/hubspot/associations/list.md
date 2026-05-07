---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot associations list

```
maton hubspot associations list [flags]
```

List every association of a given target type from a single source record
(GET /crm/v4/objects/{from}/{id}/associations/{to}).

--from is a type:id pair like "contacts:12345"; --to is just the target
object type ("companies", "deals", etc.) since the endpoint returns all
matching links, not a single one.


### Options


<dl class="flags">
	<dt>
		<code>--after &lt;string&gt;</code></dt>
	<dd>Pagination cursor from a previous response</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--from &lt;string&gt;</code></dt>
	<dd>Source object as type:id (required, e.g. contacts:12345)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 10)</code></dt>
	<dd>Max results per page</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--to &lt;string&gt;</code></dt>
	<dd>Target object type (required, e.g. companies)</dd>
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
$ maton hubspot associations list --from contacts:12345 --to companies
$ maton hubspot associations list --from deals:99999 --to contacts --paginate --json
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot associations](/manual/maton/hubspot/associations)
