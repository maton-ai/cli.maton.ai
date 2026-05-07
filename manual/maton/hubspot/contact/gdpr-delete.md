---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton hubspot contact gdpr-delete

Permanently delete a contact and prevent re-creation under the same email (irreversible)

```
maton hubspot contact gdpr-delete [<id>] [flags]
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
		<code>--email &lt;string&gt;</code></dt>
	<dd>Look up the contact by email instead of id</dd>

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

	<dt>
		<code>--yes</code></dt>
	<dd>Confirm without prompting</dd>
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
$ maton hubspot contact gdpr-delete 12345 --yes
$ maton hubspot contact gdpr-delete --email user@example.com --yes
{% endraw %}{% endhighlight %}

### See also

* [maton hubspot contact](/manual/maton/hubspot/contact)
