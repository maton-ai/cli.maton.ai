---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads campaign update

```
maton google-ads campaign update [flags]
```

Update one or more fields on a campaign by POSTing an update operation to customers/{id}/campaigns:mutate. The update mask is built from whichever mutating flags you pass — fields you omit are left untouched.

At least one mutating flag (--name, --status) must be set.


### Options


<dl class="flags">
	<dt>
		<code>--campaign-id &lt;string&gt;</code></dt>
	<dd>Campaign ID to update (required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-c</code>, 
		<code>--customer-id &lt;string&gt;</code></dt>
	<dd>Google Ads customer ID (required)</dd>

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
		<code>--name &lt;string&gt;</code></dt>
	<dd>New campaign name</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--status &lt;string&gt;</code></dt>
	<dd>New status: ENABLED, PAUSED, REMOVED</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt>
		<code>--login-customer-id &lt;string&gt;</code></dt>
	<dd>Manager account ID for MCC access (forwarded as login-customer-id header)</dd>

	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-ads campaign update -c 1234567890 --campaign-id 99999 --status ENABLED
$ maton google-ads campaign update -c 1234567890 --campaign-id 99999 --name "Launch (renamed)"
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads campaign](/manual/maton/google-ads/campaign)
