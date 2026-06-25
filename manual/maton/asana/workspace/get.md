---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana workspace get

Get a workspace by gid

```
maton asana workspace get <workspace-gid> [flags]
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

	<dt>
		<code>--opt-fields &lt;string&gt;</code></dt>
	<dd>Comma-separated fields to return</dd>

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

 maton asana workspaces view, maton asana workspace view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton asana workspace get 12345
{% endraw %}{% endhighlight %}

### See also

* [maton asana workspace](/manual/maton/asana/workspace)
