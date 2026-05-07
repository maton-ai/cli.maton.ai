---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce record create

```
maton salesforce record create [flags]
```

Create a record (POST /sobjects/{type}) when --data is a JSON object,
or up to 200 records (POST /composite/sobjects) when --data is a JSON
array. In array mode each record must include its own attributes.type
and the --type flag is ignored; pass --all-or-none to roll back the
whole batch if any record fails.


### Options


<dl class="flags">
	<dt>
		<code>--all-or-none</code></dt>
	<dd>Batch only: roll back the entire batch if any record fails</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--data &lt;string&gt;</code></dt>
	<dd>Record fields as JSON object, or JSON array of records for batch</dd>

	<dt><code>-F</code>, 
		<code>--data-file &lt;string&gt;</code></dt>
	<dd>Read JSON record fields from a file (use - for stdin)</dd>

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

	<dt>
		<code>--type &lt;string&gt;</code></dt>
	<dd>sObject type (required when --data is a JSON object; ignored when array)</dd>
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
$ maton salesforce record create --type Account --data-file account.json
$ cat account.json | maton salesforce record create --type Account -F -
$ maton salesforce record create -F records.json
$ maton salesforce record create --all-or-none -F records.json
{% endraw %}{% endhighlight %}

### See also

* [maton salesforce record](/manual/maton/salesforce/record)
