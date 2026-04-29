---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton connection view

```
maton connection view <id> [flags]
```

Show details for an app connection by its ID.

### Options


<dl class="flags">
	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

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


### JSON Fields

`app`, `connectionId`, `creationTime`, `lastUpdatedTime`, `metadata`, `method`, `status`, `url`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton connection view conn_abc123
$ maton connection view conn_abc123 --json status,url
$ maton connection view conn_abc123 --json metadata --jq '.metadata.team'
{% endraw %}{% endhighlight %}

### See also

* [maton connection](./maton_connection)
