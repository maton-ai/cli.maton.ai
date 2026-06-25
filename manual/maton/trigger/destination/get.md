---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger destination get

Show details for a destination

```
maton trigger destination get <destination-id> --trigger <trigger-id> [flags]
```

### Options


<dl class="flags">
	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--trigger &lt;string&gt;</code></dt>
	<dd>Trigger ID this resource belongs to (required)</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton trigger destinations view, maton trigger destination view

### JSON Fields

`body_template`, `created_at`, `destination_id`, `headers`, `method`, `name`, `reason`, `signing_secret`, `status`, `updated_at`, `url`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger destination get dst_123 --trigger trg_abc123
$ maton trigger destination get dst_123 --trigger trg_abc123 --json url,status
{% endraw %}{% endhighlight %}

### See also

* [maton trigger destination](/manual/maton/trigger/destination)
