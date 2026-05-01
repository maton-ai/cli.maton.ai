---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe customer list

List customers

```
maton stripe customer list [flags]
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
	<dd>Filter by exact email</dd>

	<dt>
		<code>--ending-before &lt;string&gt;</code></dt>
	<dd>Cursor for previous page (customer ID)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 10)</code></dt>
	<dd>Max results per page (1-100)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--starting-after &lt;string&gt;</code></dt>
	<dd>Cursor for next page (customer ID)</dd>

	<dt>
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
$ maton stripe customer list
$ maton stripe customer list --email alice@example.com
$ maton stripe customer list -L 50 --starting-after cus_123
$ maton stripe customer list --paginate
$ maton stripe customer list --format text
{% endraw %}{% endhighlight %}

### See also

* [maton stripe customer](/manual/maton/stripe/customer)
