---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger list

```
maton trigger list [flags]
```

List the triggers in your Maton account. Use --source / --status to narrow the results.

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
	<dd>Maximum number of triggers to fetch (0 = no limit)</dd>

	<dt>
		<code>--source &lt;string&gt;</code></dt>
	<dd>Filter by source app</dd>

	<dt>
		<code>--status &lt;string&gt;</code></dt>
	<dd>Filter by status: {ENABLED|DISABLED}</dd>

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

maton trigger ls

### JSON Fields

`connection_id`, `created_at`, `description`, `destinations`, `event_type`, `name`, `parameters`, `reason`, `source`, `status`, `trigger_id`, `updated_at`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger list
$ maton trigger list --source github
$ maton trigger list --status ENABLED
$ maton trigger list --json trigger_id,source,status
{% endraw %}{% endhighlight %}

### See also

* [maton trigger](/manual/maton/trigger)
