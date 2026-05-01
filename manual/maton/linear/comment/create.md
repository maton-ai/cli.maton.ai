---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear comment create

Add a comment to an issue

```
maton linear comment create [flags]
```

### Options


<dl class="flags">
	<dt><code>-b</code>, 
		<code>--body &lt;string&gt;</code></dt>
	<dd>Comment body (markdown) (one of --body/--text-from-file)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--issue &lt;string&gt;</code></dt>
	<dd>Issue identifier (e.g. MTN-527) or UUID (required)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;file&gt;</code></dt>
	<dd>Read body from file (or `-` for stdin) (one of --body/--text-from-file)</dd>
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
$ maton linear comment create --issue MTN-527 -b 'Looking into this'
$ cat note.md | maton linear comment create --issue MTN-527 -F -
{% endraw %}{% endhighlight %}

### See also

* [maton linear comment](/manual/maton/linear/comment)
