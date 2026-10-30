---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton bridge update

```
maton bridge update <bridge-id> [flags]
```

Update a bridge by its ID.

### Options


<dl class="flags">
	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>New name</dd>

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


### JSON Fields

`bridge_id`, `created_at`, `ip`, `name`, `status`, `updated_at`, `url`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton bridge update 3f2b9c1e-5d4a-4e8b-9a7c-1b2d3e4f5a6b --name office
{% endraw %}{% endhighlight %}

### See also

* [maton bridge](/manual/maton/bridge)
