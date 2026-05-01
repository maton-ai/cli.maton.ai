---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton connection list

```
maton connection list [<app>] [flags]
```

List the app connections in your Maton account. Pass an app name to filter to that app, and/or use --status / --method to narrow further.

### Options


<dl class="flags">
	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 30)</code></dt>
	<dd>Maximum number of connections to fetch</dd>

	<dt>
		<code>--method &lt;string&gt;</code></dt>
	<dd>Filter by connection method: {API_KEY|BASIC|JWT|OAUTH1|OAUTH2|MCP}</dd>

	<dt>
		<code>--status &lt;string&gt;</code></dt>
	<dd>Filter by connection status: {ACTIVE|PENDING|FAILED}</dd>

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

maton connection ls

### JSON Fields

`app`, `connectionId`, `creationTime`, `lastUpdatedTime`, `metadata`, `method`, `status`, `url`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton connection list
$ maton connection list google-mail
$ maton connection list --status ACTIVE
$ maton connection list google-mail --status ACTIVE
{% endraw %}{% endhighlight %}

### See also

* [maton connection](/manual/maton/connection)
