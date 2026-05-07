---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube comment list

List comment threads on a video

```
maton youtube comment list [flags]
```

### Options


<dl class="flags">
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

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 20)</code></dt>
	<dd>Max results (1-100)</dd>

	<dt>
		<code>--order &lt;string&gt; (default &#34;relevance&#34;)</code></dt>
	<dd>Sort: relevance, time</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-v</code>, 
		<code>--video &lt;string&gt;</code></dt>
	<dd>Video ID to list comments for (required)</dd>
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
$ maton youtube comment list --video dQw4w9WgXcQ
$ maton youtube comment list --video dQw4w9WgXcQ --order time --limit 100
{% endraw %}{% endhighlight %}

### See also

* [maton youtube comment](/manual/maton/youtube/comment)
