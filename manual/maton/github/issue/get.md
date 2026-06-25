---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue get

Get an issue

```
maton github issue get <number-or-url> [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--comments</code></dt>
	<dd>Fetch and append the issue&#39;s comments</dd>

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

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

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


### ALIASES

 maton github issues view, maton github issue view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github issue get 123 --repo maton-ai/cli
$ maton github issue get 123 --repo maton-ai/cli --comments
$ maton github issue get https://github.com/maton-ai/cli/issues/123
{% endraw %}{% endhighlight %}

### See also

* [maton github issue](/manual/maton/github/issue)
