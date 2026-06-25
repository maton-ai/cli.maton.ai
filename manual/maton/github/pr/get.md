---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr get

Get a pull request

```
maton github pr get <number-or-url> [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--comments</code></dt>
	<dd>Fetch and append issue comments on the PR</dd>

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

 maton github prs view,  maton github pull-request view, maton github pr view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github pr get 123 --repo maton-ai/cli
$ maton github pr get 123 --repo maton-ai/cli --comments
{% endraw %}{% endhighlight %}

### See also

* [maton github pr](/manual/maton/github/pr)
