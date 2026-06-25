---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger event replay

```
maton trigger event replay <event-id> --trigger <trigger-id> [flags]
```

Re-deliver an event to the trigger's destinations. A new event is recorded for the replay.

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


### JSON Fields

`deliveries`, `event_id`, `payload`, `received_at`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger event replay evt_123 --trigger trg_abc123
{% endraw %}{% endhighlight %}

### See also

* [maton trigger event](/manual/maton/trigger/event)
