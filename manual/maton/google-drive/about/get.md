---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive about get

Show authenticated user, storage quota, and feature flags

```
maton google-drive about get [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--fields &lt;string&gt; (default &#34;user,storageQuota,maxImportSizes,maxUploadSize,appInstalled,canCreateDrives&#34;)</code></dt>
	<dd>Partial-response field mask</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

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
$ maton google-drive about get
$ maton google-drive about get --json
$ maton google-drive about get --fields 'user,storageQuota'
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive about](/manual/maton/google-drive/about)
