---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive item create-folder

Create a new folder under the root, a parent path, or a parent ID

```
maton one-drive item create-folder <name> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--conflict &lt;string&gt; (default &#34;fail&#34;)</code></dt>
	<dd>Conflict behavior: fail, replace, rename</dd>

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
		<code>--parent-id &lt;string&gt;</code></dt>
	<dd>Parent folder ID</dd>

	<dt>
		<code>--path &lt;string&gt;</code></dt>
	<dd>Parent folder path (e.g. Documents/Projects)</dd>

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
$ maton one-drive item create-folder Reports
$ maton one-drive item create-folder Reports --path Documents/Projects
$ maton one-drive item create-folder Reports --parent-id 01ABCDEF
$ maton one-drive item create-folder Reports --conflict rename
{% endraw %}{% endhighlight %}

### See also

* [maton one-drive item](/manual/maton/one-drive/item)
