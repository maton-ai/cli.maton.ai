---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function get

```
maton function get <function-id> [flags]
```

Show details for a function by its ID, including the URL it answers on.

### Options


<dl class="flags">
	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

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

 maton functions view, maton function view

### JSON Fields

`account_id`, `created_at`, `description`, `function_id`, `name`, `network_policy`, `runtime`, `star_count`, `updated_at`, `url`, `version`, `view_count`, `visibility`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton function get 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function get 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --json url,version
{% endraw %}{% endhighlight %}

### See also

* [maton function](/manual/maton/function)
