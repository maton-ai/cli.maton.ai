---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger destination update

Update a trigger's destination

```
maton trigger destination update <destination-id> --trigger <trigger-id> [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--body-template &lt;string&gt;</code></dt>
	<dd>New body template</dd>

	<dt>
		<code>--header &lt;stringArray&gt;</code></dt>
	<dd>Header key=value pair (repeatable, replaces all headers)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt>
		<code>--method &lt;string&gt;</code></dt>
	<dd>New HTTP method</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>New name</dd>

	<dt>
		<code>--status &lt;string&gt;</code></dt>
	<dd>New status: {ENABLED|DISABLED}</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-t</code>, 
		<code>--trigger &lt;string&gt;</code></dt>
	<dd>Trigger ID this resource belongs to (required)</dd>

	<dt>
		<code>--url &lt;string&gt;</code></dt>
	<dd>New destination URL, must start with https://</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### JSON Fields

`body_template`, `created_at`, `destination_id`, `headers`, `method`, `name`, `reason`, `signing_secret`, `status`, `updated_at`, `url`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger destination update dst_123 --trigger trg_abc123 --url https://httpbin.org/post
$ maton trigger destination update dst_123 --trigger trg_abc123 --status DISABLED
{% endraw %}{% endhighlight %}

### See also

* [maton trigger destination](/manual/maton/trigger/destination)
