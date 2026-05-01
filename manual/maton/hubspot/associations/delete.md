---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot associations delete

Remove all associations between two CRM objects

```
maton hubspot associations delete [flags]
```

### Options


<dl class="flags">
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
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton hubspot associations archive, maton hubspot association archive

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton hubspot associations delete --from contacts:12345 --to companies:67890
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot associations](/manual/maton/hubspot/associations)
