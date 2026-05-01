---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive drive list

List shared drives

```
maton google-drive drive list [flags]
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

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-L</code>, 
		<code>--page-size &lt;int&gt; (default 100)</code></dt>
	<dd>Max drives per page (1-100)</dd>

	<dt>
		<code>--page-token &lt;string&gt;</code></dt>
	<dd>Pagination token</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-Q</code>, 
		<code>--query &lt;string&gt;</code></dt>
	<dd>Drive query expression</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--use-domain-admin-access</code></dt>
	<dd>Issue the request as a domain administrator</dd>
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
$ maton google-drive drive list
$ maton google-drive drive list --format text --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive drive](/manual/maton/google-drive/drive)
