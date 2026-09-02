---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function list

```
maton function list [flags]
```

List the functions in your Maton account.

With `--owner ALL` the listing covers the public corpus rather than your
account, so the only visibility it can return is `PUBLIC`.


### Options


<dl class="flags">
	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Maximum number of functions to fetch (0 = no limit)</dd>

	<dt>
		<code>--owner &lt;string&gt;</code></dt>
	<dd>Whose functions to list: {SELF|ALL}</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--visibility &lt;string&gt;</code></dt>
	<dd>Filter by visibility: {PRIVATE|PUBLIC|UNLISTED}</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton functions ls, maton function ls

### JSON Fields

`account_id`, `description`, `function_id`, `name`, `runtime`, `star_count`, `url`, `view_count`, `visibility`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton function list
$ maton function list --visibility PUBLIC
$ maton function list --owner ALL
$ maton function list --json function_id,name,url
{% endraw %}{% endhighlight %}

### See also

* [maton function](/manual/maton/function)
