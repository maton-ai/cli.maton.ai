---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce composite call

```
maton salesforce composite call [flags]
```

POST a {"compositeRequest":[...]} payload to /composite. Subrequests run
in order and can reference each other's results via @{referenceId.field}.
Up to 25 subrequests per call.


### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--data &lt;string&gt;</code></dt>
	<dd>Payload as JSON (e.g. &#39;{&#34;compositeRequest&#34;:[...]}&#39;)</dd>

	<dt><code>-F</code>, 
		<code>--data-file &lt;string&gt;</code></dt>
	<dd>Read JSON payload from a file (use - for stdin)</dd>

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
$ maton salesforce composite call -F composite.json
$ cat composite.json | maton salesforce composite call -F -
{% endraw %}{% endhighlight %}

### See also

* [maton salesforce composite](/manual/maton/salesforce/composite)
