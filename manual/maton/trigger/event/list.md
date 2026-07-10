---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger event list

List events received by a trigger

```
maton trigger event list --trigger <trigger-id> [flags]
```

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
	<dd>Maximum number of events to fetch (0 = no limit)</dd>

	<dt>
		<code>--since &lt;string&gt;</code></dt>
	<dd>Only list events received after this event ID</dd>

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

 maton trigger events ls, maton trigger event ls

### JSON Fields

`delivery_counts`, `event_id`, `payload`, `received_at`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger event list --trigger trg_abc123
$ maton trigger event list --trigger trg_abc123 -L 50
$ maton trigger event list --trigger trg_abc123 --since evt_123
{% endraw %}{% endhighlight %}

### See also

* [maton trigger event](/manual/maton/trigger/event)
