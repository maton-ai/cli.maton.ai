---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linkedin post list

```
maton linkedin post list [flags]
```

List posts for an author. Provide either --author with a URN such as
urn:li:person:abc123 or urn:li:organization:12345, or --org-id with a
numeric organization ID (which is expanded to urn:li:organization:<id>).

### Options


<dl class="flags">
	<dt>
		<code>--author &lt;string&gt;</code></dt>
	<dd>Author URN, e.g. urn:li:person:abc123 (one of --author or --org-id required)</dd>

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
		<code>--limit &lt;int&gt; (default 10)</code></dt>
	<dd>Number of posts to return per page</dd>

	<dt>
		<code>--org-id &lt;string&gt;</code></dt>
	<dd>Numeric organization ID; expanded to urn:li:organization:&lt;id&gt; (one of --author or --org-id required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--start &lt;int&gt; (default 0)</code></dt>
	<dd>Start index for pagination</dd>

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
$ maton linkedin post list --author urn:li:person:abc123
$ maton linkedin post list --org-id 12345 --limit 50
$ maton linkedin post list --author urn:li:person:abc123 --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton linkedin post](/manual/maton/linkedin/post)
