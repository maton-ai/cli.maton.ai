---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton yahoo-mail thread get

```
maton yahoo-mail thread get <thread-id> [flags]
```

List every message in a thread across all folders, oldest first. Thread IDs are
assigned by Yahoo Mail; they are in the THREAD column of "message list" and in thread_id
from "message get --json".

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

 maton yahoo-mail threads view, maton yahoo-mail thread view

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton yahoo-mail thread get 43
$ maton yahoo-mail thread get 43 --json
{% endraw %}{% endhighlight %}

### See also

* [maton yahoo-mail thread](/manual/maton/yahoo-mail/thread)
