---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack search files

Search files across channels

```
maton slack search files <query> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--count &lt;int&gt; (default 20)</code></dt>
	<dd>Results per page</dd>

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
		<code>--page &lt;int&gt; (default 1)</code></dt>
	<dd>Page number</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--sort &lt;string&gt; (default &#34;timestamp&#34;)</code></dt>
	<dd>Sort by: score or timestamp</dd>

	<dt>
		<code>--sort-dir &lt;string&gt; (default &#34;desc&#34;)</code></dt>
	<dd>Sort direction: asc or desc</dd>

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
$ maton slack search files 'report.pdf'
{% endraw %}{% endhighlight %}

### See also

* [maton slack search](/manual/maton/slack/search)
