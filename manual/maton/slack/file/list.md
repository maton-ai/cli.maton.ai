---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack file list

List files visible to you

```
maton slack file list [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Filter by channel ID</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--count &lt;int&gt; (default 100)</code></dt>
	<dd>Max results per page</dd>

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
		<code>--page &lt;int&gt; (default 0)</code></dt>
	<dd>Page number (1-based)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--types &lt;string&gt;</code></dt>
	<dd>Comma-separated file types (e.g. images,pdfs,snippets)</dd>

	<dt>
		<code>--user &lt;string&gt;</code></dt>
	<dd>Filter by user ID</dd>
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
$ maton slack file list
$ maton slack file list --channel C0123456789
$ maton slack file list --user U0123456789 --types images,pdfs
$ maton slack file list --count 50 --page 2 --json
{% endraw %}{% endhighlight %}

### See also

* [maton slack file](/manual/maton/slack/file)
