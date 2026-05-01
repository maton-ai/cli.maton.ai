---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton connection create

```
maton connection create <app> [flags]
```

Create a connection to a third-party app. By default this opens your browser to complete the OAuth handshake and waits until the connection becomes active. Use --interactive on a headless host to skip the browser launch.

### Options


<dl class="flags">
	<dt><code>-i</code>, 
		<code>--interactive</code></dt>
	<dd>Skip launching the browser; print the URL and wait</dd>

	<dt>
		<code>--interval &lt;duration&gt; (default &#34;2s&#34;)</code></dt>
	<dd>Polling interval while waiting for the connection to become active</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt>
		<code>--method &lt;string&gt;</code></dt>
	<dd>Connection method: {API_KEY|BASIC|JWT|OAUTH1|OAUTH2|MCP}</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--timeout &lt;duration&gt; (default &#34;5m0s&#34;)</code></dt>
	<dd>Maximum time to wait for the connection to become active</dd>
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
$ maton connection create slack
$ maton connection create slack --interactive
$ maton connection create slack --method OAUTH2
$ maton connection create slack --json connectionId,status
{% endraw %}{% endhighlight %}

### See also

* [maton connection](/manual/maton/connection)
