---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube video list

List trending/popular videos by region

```
maton youtube video list [flags]
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
		<code>--limit &lt;int&gt; (default 10)</code></dt>
	<dd>Max results (1-50)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parts &lt;string&gt; (default &#34;snippet,statistics&#34;)</code></dt>
	<dd>Comma-separated parts: snippet, statistics, contentDetails, status, player</dd>

	<dt>
		<code>--region &lt;string&gt; (default &#34;US&#34;)</code></dt>
	<dd>Region code (e.g. US, KR, JP)</dd>

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
$ maton youtube video list
$ maton youtube video list --region KR --limit 25
{% endraw %}{% endhighlight %}

### See also

* [maton youtube video](./maton_youtube_video)
