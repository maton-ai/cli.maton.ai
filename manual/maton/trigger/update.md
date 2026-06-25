---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger update

```
maton trigger update <trigger-id> [flags]
```

Update a trigger's name, description, status, or parameters. Only the flags you pass are changed. To edit destinations, use `maton trigger destination update` instead.

### Options


<dl class="flags">
	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>New description</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>New name</dd>

	<dt>
		<code>--parameter &lt;stringArray&gt;</code></dt>
	<dd>Trigger parameter key=value pair (repeatable, replaces all parameters)</dd>

	<dt>
		<code>--status &lt;string&gt;</code></dt>
	<dd>New status: {ENABLED|DISABLED}</dd>

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

`connection_id`, `created_at`, `description`, `destinations`, `event_type`, `name`, `parameters`, `reason`, `source`, `status`, `trigger_id`, `updated_at`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger update trg_abc123 --name "PR opened"
$ maton trigger update trg_abc123 --status DISABLED
$ maton trigger update trg_abc123 --parameter repo=maton-ai/cli
{% endraw %}{% endhighlight %}

### See also

* [maton trigger](/manual/maton/trigger)
