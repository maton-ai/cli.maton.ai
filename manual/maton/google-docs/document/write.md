---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-docs document write

```
maton google-docs document write <document-id> [flags]
```

Insert plain text at the end of a document body via documents.batchUpdate. For rich formatting (links, headings, tables), call documents.batchUpdate directly via 'maton api'.

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
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--text &lt;string&gt;</code></dt>
	<dd>Text to append at the end of the body (one of --text/--text-from-file)</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;string&gt;</code></dt>
	<dd>Read text from a file (&#39;-&#39; for stdin) (one of --text/--text-from-file)</dd>
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
$ maton google-docs document write DOC_ID --text 'Hello, world!'
$ maton google-docs document write DOC_ID -F notes.md
$ echo 'piped text' | maton google-docs document write DOC_ID -F -
{% endraw %}{% endhighlight %}

### See also

* [maton google-docs document](/manual/maton/google-docs/document)
