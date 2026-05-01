---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linkedin post create

Create a text post on LinkedIn

```
maton linkedin post create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--article-description &lt;string&gt;</code></dt>
	<dd>Description for the shared article</dd>

	<dt>
		<code>--article-title &lt;string&gt;</code></dt>
	<dd>Title for the shared article</dd>

	<dt>
		<code>--article-url &lt;string&gt;</code></dt>
	<dd>URL to share as an article attachment</dd>

	<dt>
		<code>--author &lt;string&gt;</code></dt>
	<dd>Author URN, e.g. urn:li:person:abc123 (required)</dd>

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
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--text &lt;string&gt;</code></dt>
	<dd>Post commentary / body text (required)</dd>

	<dt>
		<code>--visibility &lt;string&gt; (default &#34;PUBLIC&#34;)</code></dt>
	<dd>Visibility: PUBLIC or CONNECTIONS</dd>
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
$ maton linkedin post create --author urn:li:person:abc123 --text 'Shipping a new feature today!'
$ maton linkedin post create --author urn:li:person:abc123 --text 'Read more' \
    --article-url https://example.com/post --article-title 'Example' --article-description 'A summary'
{% endraw %}{% endhighlight %}

### See also

* [maton linkedin post](/manual/maton/linkedin/post)
