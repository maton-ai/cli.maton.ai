---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack file upload

Upload a file and optionally share it to a channel

```
maton slack file upload [flags]
```

### Options


<dl class="flags">
	<dt><code>-c</code>, 
		<code>--channel &lt;string&gt;</code></dt>
	<dd>Channel ID to share the file in</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--file &lt;string&gt;</code></dt>
	<dd>Path to a local file to upload (required)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt>
		<code>--initial-comment &lt;string&gt;</code></dt>
	<dd>Message to post alongside the file</dd>

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
		<code>--thread-ts &lt;string&gt;</code></dt>
	<dd>Post the file as a reply in this thread</dd>

	<dt>
		<code>--title &lt;string&gt;</code></dt>
	<dd>Display title for the file</dd>
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
$ maton slack file upload --file ./report.pdf --channel C012
$ maton slack file upload --file ./notes.md --channel C012 --title 'Sprint notes' --initial-comment 'fwiw'
$ maton slack file upload --file ./trace.log --channel C012 --thread-ts 1700000000.000100
{% endraw %}{% endhighlight %}

### See also

* [maton slack file](/manual/maton/slack/file)
