---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger get

```
maton trigger get <trigger-id> [flags]
```

Show details for a trigger by its ID, including its destinations.

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

maton trigger view

### JSON Fields

`connection_id`, `created_at`, `description`, `destinations`, `event_type`, `name`, `parameters`, `reason`, `source`, `status`, `trigger_id`, `updated_at`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger get trg_abc123
$ maton trigger get trg_abc123 --json status,destinations
{% endraw %}{% endhighlight %}

### See also

* [maton trigger](/manual/maton/trigger)
