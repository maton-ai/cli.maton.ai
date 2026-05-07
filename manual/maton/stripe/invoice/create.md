---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton stripe invoice create

Create an invoice for a customer

```
maton stripe invoice create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--auto-advance &lt;string&gt;</code></dt>
	<dd>Set &#39;true&#39; or &#39;false&#39; to control auto-finalization</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--customer &lt;string&gt;</code></dt>
	<dd>Customer ID (required)</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description</dd>

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
		<code>--metadata &lt;stringArray&gt;</code></dt>
	<dd>Metadata key=value pair (repeatable)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--subscription &lt;string&gt;</code></dt>
	<dd>Subscription ID to attach</dd>

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
$ maton stripe invoice create --customer cus_123
$ maton stripe invoice create --customer cus_123 --auto-advance true --description 'March usage'
{% endraw %}{% endhighlight %}

### See also

* [maton stripe invoice](/manual/maton/stripe/invoice)
