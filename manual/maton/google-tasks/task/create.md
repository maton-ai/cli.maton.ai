---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-tasks task create

Create a new task in a list

```
maton google-tasks task create [flags]
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
		<code>--due &lt;string&gt;</code></dt>
	<dd>Due date (YYYY-MM-DD or RFC 3339)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt><code>-l</code>, 
		<code>--list &lt;string&gt;</code></dt>
	<dd>Task list ID (required)</dd>

	<dt>
		<code>--notes &lt;string&gt;</code></dt>
	<dd>Task description (max 8192 chars)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--parent &lt;string&gt;</code></dt>
	<dd>Parent task ID to create as subtask</dd>

	<dt>
		<code>--previous &lt;string&gt;</code></dt>
	<dd>Place after this sibling task ID</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--title &lt;string&gt;</code></dt>
	<dd>Task title (required, max 1024 chars)</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton google-tasks tasks insert, maton google-tasks task insert

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-tasks task create -l MTYxNzM4 --title 'Write spec'
$ maton google-tasks task create -l MTYxNzM4 --title 'Subtask' --parent OTQyNzc
$ maton google-tasks task create -l MTYxNzM4 --title 'Review' --due 2026-12-01
{% endraw %}{% endhighlight %}

### See also

* [maton google-tasks task](/manual/maton/google-tasks/task)
