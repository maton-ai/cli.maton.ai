---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive drive search

Search files and folders by name or content

```
maton one-drive drive search <query> [flags]
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

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--select &lt;string&gt;</code></dt>
	<dd>Comma-separated fields ($select)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-L</code>, 
		<code>--top &lt;int&gt; (default 0)</code></dt>
	<dd>Max results per page ($top)</dd>
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
$ maton one-drive drive search 'budget'
$ maton one-drive drive search 'report' --top 10 --select name,webUrl
$ maton one-drive drive search 'report' --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton one-drive drive](/manual/maton/one-drive/drive)
