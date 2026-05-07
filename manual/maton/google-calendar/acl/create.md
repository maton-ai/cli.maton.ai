---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar acl create

```
maton google-calendar acl create [flags]
```

Create an ACL rule. --role is one of `none`, `freeBusyReader`, `reader`, `writer`, `owner`. --scope-type is `user`, `group`, `domain`, or `default`; --scope is the email/domain (omit for default).

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--calendar &lt;string&gt;</code></dt>
	<dd>Calendar ID (required)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

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

	<dt>
		<code>--role &lt;string&gt;</code></dt>
	<dd>Access role (required)</dd>

	<dt>
		<code>--scope &lt;string&gt;</code></dt>
	<dd>Email or domain identifying the principal (omit only when --scope-type=default)</dd>

	<dt>
		<code>--scope-type &lt;string&gt; (default &#34;user&#34;)</code></dt>
	<dd>user|group|domain|default</dd>

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
$ maton google-calendar acl create -c primary --role reader --scope alice@example.com
$ maton google-calendar acl create -c primary --role reader --scope-type domain --scope example.com
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar acl](/manual/maton/google-calendar/acl)
