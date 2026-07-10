---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot deal search

```
maton hubspot deal search [flags]
```

Search HubSpot deals using one or more filters. Filters are combined with AND inside a single filterGroup. Operators: EQ, NEQ, LT, LTE, GT, GTE, CONTAINS_TOKEN, NOT_CONTAINS_TOKEN, HAS_PROPERTY, NOT_HAS_PROPERTY. Valueless operators (HAS_PROPERTY, NOT_HAS_PROPERTY) take the form propertyName:operator.

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
		<code>--filter &lt;stringArray&gt;</code></dt>
	<dd>Filter as propertyName:operator:value (required, at least one)</dd>

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

	<dt>
		<code>--properties &lt;string&gt;</code></dt>
	<dd>Comma-separated properties to return</dd>

	<dt><code>-t</code>, 
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
$ maton hubspot deal search --filter dealstage:EQ:closedwon
$ maton hubspot deal search --filter amount:GT:1000 --properties dealname,amount
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot deal](/manual/maton/hubspot/deal)
