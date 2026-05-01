---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce record update

Update an existing record

```
maton salesforce record update <id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--data &lt;string&gt;</code></dt>
	<dd>Fields to update as JSON (e.g. &#39;{&#34;Phone&#34;:&#34;&#43;1234567890&#34;}&#39;)</dd>

	<dt><code>-F</code>, 
		<code>--data-from-file &lt;string&gt;</code></dt>
	<dd>Read JSON fields from a file (use - for stdin)</dd>

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
		<code>--type &lt;string&gt;</code></dt>
	<dd>sObject type (required, e.g. Contact, Account, Lead, Opportunity, Case)</dd>
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
$ maton salesforce record update 0035g00000XYZ --type Contact --data '{"Phone":"+1234567890"}'
$ maton salesforce record update 0035g00000XYZ --type Contact -F update.json
{% endraw %}{% endhighlight %}

### See also

* [maton salesforce record](/manual/maton/salesforce/record)
