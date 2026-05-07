---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton outlook contact create

Create a contact

```
maton outlook contact create [flags]
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
		<code>--email &lt;strings&gt;</code></dt>
	<dd>Email address (repeatable)</dd>

	<dt>
		<code>--given-name &lt;string&gt;</code></dt>
	<dd>Given (first) name (required)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--surname &lt;string&gt;</code></dt>
	<dd>Surname (last name) (required)</dd>

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
$ maton outlook contact create --given-name Alice --surname Smith --email alice@example.com
$ maton outlook contact create --given-name Bob --surname Jones --email bob@example.com --email bob.work@example.com
{% endraw %}{% endhighlight %}

### See also

* [maton outlook contact](/manual/maton/outlook/contact)
