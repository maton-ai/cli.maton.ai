---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton connection reauthorize

```
maton connection reauthorize <id> [flags]
```

Reauthorize a FAILED or PENDING connection in place. It keeps its connection ID, so scripts and settings that use that ID keep working. By default this opens your browser to authorize the app again and waits until the connection becomes active. For iCloud Mail and Yahoo Mail it waits until the new app password is accepted, then shows how the mailbox will send. Use --interactive on a headless host to skip the browser launch. An ACTIVE connection doesn't need reauthorizing.

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

`app`, `connection_id`, `creation_time`, `last_updated_time`, `metadata`, `method`, `status`, `status_reason`, `url`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton connection reauthorize conn_abc123
$ maton connection reauthorize conn_abc123 --interactive
$ maton connection reauthorize conn_abc123 --json connection_id,status,url
{% endraw %}{% endhighlight %}

### See also

* [maton connection](/manual/maton/connection)
