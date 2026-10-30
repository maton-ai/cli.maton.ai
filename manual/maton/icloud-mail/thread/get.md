---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton icloud-mail thread get

```
maton icloud-mail thread get <thread-id> [flags]
```

List every message in a thread across all folders, oldest first. Thread IDs are in
the THREAD column of "message list" and in thread_id from "message get --json".

iCloud Mail assigns no thread IDs, so a thread ID is the Message-ID of the
conversation's first message, as replies name it in their References header.
Passing the message_id of any message in the conversation also works.

Each message is listed as a summary; use "message get" for its body.


### Options


<dl class="flags">
	<dt>
		<code>--bridge &lt;string&gt;</code></dt>
	<dd>Bridge ID to send the request through (Maton-Bridge header); see &#34;maton bridge list&#34;</dd>

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


### ALIASES

 maton icloud-mail threads view, maton icloud-mail thread view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton icloud-mail thread get CAAJQadFONrw0YUF4gQGCOvbGq0@mail.gmail.com
$ maton icloud-mail thread get CAAJQadFONrw0YUF4gQGCOvbGq0@mail.gmail.com --json
{% endraw %}{% endhighlight %}

### See also

* [maton icloud-mail thread](/manual/maton/icloud-mail/thread)
