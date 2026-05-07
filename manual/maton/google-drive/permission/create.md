---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive permission create

```
maton google-drive permission create [flags]
```

Grant a permission. --type is one of user, group, domain, anyone. --role is reader, commenter, writer, fileOrganizer, organizer, owner. user/group requires --email-address; domain requires --domain.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--domain &lt;string&gt;</code></dt>
	<dd>Domain name (for type=domain)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--email-address &lt;string&gt;</code></dt>
	<dd>Email address (for user/group)</dd>

	<dt>
		<code>--email-message &lt;string&gt;</code></dt>
	<dd>Custom message for the notification email</dd>

	<dt><code>-f</code>, 
		<code>--file &lt;string&gt;</code></dt>
	<dd>File or folder ID (required)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--no-notification</code></dt>
	<dd>Skip the notification email (overrides --send-notification-email)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--role &lt;string&gt;</code></dt>
	<dd>Role: reader, commenter, writer, fileOrganizer, organizer, owner (required)</dd>

	<dt>
		<code>--send-notification-email (default true)</code></dt>
	<dd>Send a notification email when granting access</dd>

	<dt>
		<code>--supports-all-drives</code></dt>
	<dd>Set when the file lives in a shared drive</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--transfer-ownership</code></dt>
	<dd>Required when --role=owner</dd>

	<dt>
		<code>--type &lt;string&gt;</code></dt>
	<dd>Grantee type: user, group, domain, anyone (required)</dd>
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
$ maton google-drive permission create -f 1aBcD... --type user --role writer --email-address alice@acme.com
$ maton google-drive permission create -f 1aBcD... --type anyone --role reader
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive permission](/manual/maton/google-drive/permission)
