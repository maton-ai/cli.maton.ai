---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-ads query

```
maton google-ads query [flags]
```

POSTs a GAQL query to googleAds:search. Either provide --gaql with a complete query string, or pass --resource (with optional --fields, --where, --order-by, --limit) to compose one. When --fields is omitted the default is "<resource>.id, <resource>.name".

--paginate follows nextPageToken to concatenate all pages. For very large result sets prefer "query-stream".


### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-c</code>, 
		<code>--customer-id &lt;string&gt;</code></dt>
	<dd>Google Ads customer ID (required)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--fields &lt;string&gt;</code></dt>
	<dd>Comma-separated fields to select</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--gaql &lt;string&gt;</code></dt>
	<dd>Raw GAQL query string</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>LIMIT number of results (0 = no limit)</dd>

	<dt>
		<code>--order-by &lt;string&gt;</code></dt>
	<dd>ORDER BY field</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--resource &lt;string&gt;</code></dt>
	<dd>GAQL resource (e.g. campaign, ad_group, keyword_view)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--where &lt;string&gt;</code></dt>
	<dd>WHERE clause (e.g. &#34;campaign.status != &#39;REMOVED&#39;&#34;)</dd>
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
$ maton google-ads query -c 1234567890 --gaql 'SELECT campaign.id FROM campaign'
$ maton google-ads query -c 1234567890 --resource campaign --fields 'campaign.id, campaign.name' -L 10
$ maton google-ads query -c 1234567890 --resource campaign --paginate
{% endraw %}{% endhighlight %}

### See also

* [maton google-ads](./maton_google-ads)
