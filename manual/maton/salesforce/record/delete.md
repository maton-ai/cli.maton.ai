---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce record delete

```
maton salesforce record delete <id> [<id>...] [flags]
```

Delete a single record (DELETE /sobjects/{type}/{id}).

When more than one ID is provided, the request is dispatched in one call
to /composite/sobjects?ids=... — up to 200 IDs. Each ID encodes its own
sObject type, so --type is ignored in batch mode. Set --all-or-none to
roll back the whole batch if any delete fails.


### Options


<dl class="flags">
	<dt>
		<code>--all-or-none</code></dt>
	<dd>With multiple IDs: roll back the entire batch if any delete fails</dd>

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
		<code>--type &lt;string&gt;</code></dt>
	<dd>sObject type (required for single delete; ignored with multiple IDs)</dd>
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
$ maton salesforce record delete 0035g00000XYZ --type Contact
$ maton salesforce record delete 0035g00000A 0035g00000B 0035g00000C
$ maton salesforce record delete 0035g00000A 0035g00000B --all-or-none
{% endraw %}{% endhighlight %}

### See also

* [maton salesforce record](/manual/maton/salesforce/record)
