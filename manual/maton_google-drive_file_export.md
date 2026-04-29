---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive file export

```
maton google-drive file export <file-id> [flags]
```

Export a Google-native document to --mime-type (e.g. 'application/pdf', 'text/csv', 'text/plain'). Writes to --output, or stdout when --output is "-".

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

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
		<code>--mime-type &lt;string&gt;</code></dt>
	<dd>Target MIME type (required)</dd>

	<dt><code>-o</code>, 
		<code>--output &lt;string&gt;</code></dt>
	<dd>Local path to write to (&#39;-&#39; for stdout) (required)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
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
$ maton google-drive file export 1aBcD... --mime-type application/pdf --output ./doc.pdf
$ maton google-drive file export 1aBcD... --mime-type text/csv --output -
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive file](./maton_google-drive_file)
