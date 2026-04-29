---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack channel list

List channels you can see

```
maton slack channel list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--cursor &lt;string&gt;</code></dt>
	<dd>Pagination cursor</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--exclude-archived</code></dt>
	<dd>Hide archived channels</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 100)</code></dt>
	<dd>Max results per page</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--types &lt;string&gt; (default &#34;public_channel,private_channel&#34;)</code></dt>
	<dd>Channel types: public_channel,private_channel,im,mpim</dd>
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
$ maton slack channel list
$ maton slack channel list --types public_channel,private_channel,im,mpim --limit 50
$ maton slack channel list --format text
$ maton slack channel list --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton slack channel](./maton_slack_channel)
