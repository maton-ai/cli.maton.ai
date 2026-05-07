---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube subscription list

```
maton youtube subscription list [flags]
```

List subscriptions on your account (default), or a specific channel's
subscriptions with --channel.

Pass --for-channel <channelId> to check whether the requesting account
is subscribed to that channel — the response is empty when no
subscription exists.


### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>List subscriptions for this channel ID (default: your own)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--for-channel &lt;string&gt;</code></dt>
	<dd>Filter results to subscriptions that point at this channel ID (use to check if subscribed)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 25)</code></dt>
	<dd>Max results (1-50)</dd>

	<dt>
		<code>--order &lt;string&gt;</code></dt>
	<dd>Sort: alphabetical, relevance, unread</dd>

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
$ maton youtube subscription list
$ maton youtube subscription list --paginate
$ maton youtube subscription list --channel UCBJycsmduvYEL83R_U4JriQ
$ maton youtube subscription list --for-channel UCBJycsmduvYEL83R_U4JriQ
{% endraw %}{% endhighlight %}

### See also

* [maton youtube subscription](/manual/maton/youtube/subscription)
