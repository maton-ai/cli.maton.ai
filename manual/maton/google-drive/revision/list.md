---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive revision list

List revisions of a file

```
maton google-drive revision list [flags]
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
		<code>--fields &lt;string&gt;</code></dt>
	<dd>Partial-response field mask</dd>

	<dt><code>-f</code>, 
		<code>--file &lt;string&gt;</code></dt>
	<dd>File ID (required)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--page-size &lt;int&gt; (default 200)</code></dt>
	<dd>Max revisions per page (1-1000)</dd>

	<dt>
		<code>--page-token &lt;string&gt;</code></dt>
	<dd>Pagination token</dd>

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
$ maton google-drive revision list -f 1aBcD... --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive revision](/manual/maton/google-drive/revision)
