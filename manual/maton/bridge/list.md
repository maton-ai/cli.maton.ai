---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton bridge list

```
maton bridge list [flags]
```

List bridges in your account. To use a bridge for a gateway request, pass --bridge <bridge-id> to maton api or set the Maton-Bridge: <bridge_id> header.

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

maton bridge ls

### JSON Fields

`bridge_id`, `created_at`, `ip`, `name`, `status`, `updated_at`, `url`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton bridge list
$ maton bridge list --json bridge_id
{% endraw %}{% endhighlight %}

### See also

* [maton bridge](/manual/maton/bridge)
