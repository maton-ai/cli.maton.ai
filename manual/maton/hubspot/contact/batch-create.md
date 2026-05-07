---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot contact batch-create

```
maton hubspot contact batch-create [flags]
```

Send a JSON array of {"properties":{...}} objects; HubSpot wraps it as {"inputs":[...]}.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--data &lt;string&gt;</code></dt>
	<dd>JSON array of {&#34;properties&#34;:{...}} objects (required)</dd>

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
$ maton hubspot contact batch-create --data '[{"properties":{"email":"a@b.com"}},{"properties":{"email":"c@d.com"}}]'
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot contact](/manual/maton/hubspot/contact)
