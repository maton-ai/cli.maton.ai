---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe subscription update

Update a subscription

```
maton stripe subscription update <id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--cancel-at-period-end &lt;string&gt;</code></dt>
	<dd>Set to &#39;true&#39; or &#39;false&#39;</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

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
		<code>--metadata &lt;stringArray&gt;</code></dt>
	<dd>Metadata key=value pair (repeatable)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
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
$ maton stripe subscription update sub_123 --metadata renewed=true
$ maton stripe subscription update sub_123 --cancel-at-period-end true
{% endraw %}{% endhighlight %}

### See also

* [maton stripe subscription](/manual/maton/stripe/subscription)
