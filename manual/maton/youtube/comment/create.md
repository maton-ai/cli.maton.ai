---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube comment create

```
maton youtube comment create [flags]
```

Post a comment. Use --video to start a new top-level thread on a
video, or --parent to reply to an existing comment. Exactly one of
--video or --parent is required.


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

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent &lt;string&gt;</code></dt>
	<dd>Reply to this top-level comment ID</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--text &lt;string&gt;</code></dt>
	<dd>Comment body (required)</dd>

	<dt><code>-v</code>, 
		<code>--video &lt;string&gt;</code></dt>
	<dd>Post a top-level comment on this video ID</dd>
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
$ maton youtube comment create --video dQw4w9WgXcQ --text "Great video!"
$ maton youtube comment create --parent <commentId> --text "I agree"
{% endraw %}{% endhighlight %}

### See also

* [maton youtube comment](/manual/maton/youtube/comment)
