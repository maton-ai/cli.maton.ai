---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce record create

Create a new record

```
maton salesforce record create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--data &lt;string&gt;</code></dt>
	<dd>Record fields as JSON (e.g. &#39;{&#34;FirstName&#34;:&#34;John&#34;,&#34;LastName&#34;:&#34;Doe&#34;}&#39;)</dd>

	<dt><code>-F</code>, 
		<code>--data-from-file &lt;string&gt;</code></dt>
	<dd>Read JSON record fields from a file (use - for stdin)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--type &lt;string&gt;</code></dt>
	<dd>sObject type (required, e.g. Contact, Account, Lead, Opportunity, Case)</dd>
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
$ maton salesforce record create --type Contact --data '{"FirstName":"John","LastName":"Doe"}'
$ maton salesforce record create --type Account --data-from-file account.json
$ cat account.json | maton salesforce record create --type Account -F -
{% endraw %}{% endhighlight %}

### See also

* [maton salesforce record](/manual/maton/salesforce/record)
