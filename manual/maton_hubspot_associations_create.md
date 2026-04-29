---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot associations create

```
maton hubspot associations create [flags]
```

Link two HubSpot CRM records via the v4 associations API.

Without --type, uses the default (built-in) association for the object pair
(PUT /crm/v4/objects/{from}/{id}/associations/default/{to}/{id}).

With --type, creates a typed association
(PUT /crm/v4/objects/{from}/{id}/associations/{to}/{id} with an
associationCategory + associationTypeId body).


### Options


<dl class="flags">
	<dt>
		<code>--category &lt;string&gt; (default &#34;HUBSPOT_DEFINED&#34;)</code></dt>
	<dd>Association category: HUBSPOT_DEFINED or USER_DEFINED</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--from &lt;string&gt;</code></dt>
	<dd>Source object as type:id (required, e.g. contacts:12345)</dd>

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
		<code>--to &lt;string&gt;</code></dt>
	<dd>Target object as type:id (required, e.g. companies:67890)</dd>

	<dt>
		<code>--type &lt;int&gt; (default 0)</code></dt>
	<dd>associationTypeId (omit to use the default association for this object pair)</dd>
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
$ maton hubspot associations create --from contacts:12345 --to companies:67890
$ maton hubspot associations create --from contacts:12345 --to deals:99999 --type 4
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot associations](./maton_hubspot_associations)
