---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger event watch

```
maton trigger event watch --trigger <trigger-id> [flags]
```

Print each new event a trigger receives, starting from now, until interrupted with Ctrl-C.

With --json the stream emits newline-delimited JSON (one object per line) for piping into jq or a shell loop.

With --exec the given command runs once per event via "sh -c", with the event JSON on stdin and its ID in MATON_EVENT_ID. The last processed event ID is checkpointed per trigger, so restarting resumes after it and an interrupted batch never re-runs handled events.


### Options


<dl class="flags">
	<dt>
		<code>--exec &lt;string&gt;</code></dt>
	<dd>Run a shell command for each new event (event JSON on stdin)</dd>

	<dt>
		<code>--exit-status</code></dt>
	<dd>Exit non-zero on a poll error instead of logging and continuing</dd>

	<dt>
		<code>--interval &lt;duration&gt; (default &#34;2s&#34;)</code></dt>
	<dd>Polling interval</dd>

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

`delivery_counts`, `event_id`, `payload`, `received_at`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger event watch --trigger trg_abc123
$ maton trigger event watch -t trg_abc123 --exec ./handle.sh
$ maton trigger event watch -t trg_abc123 --json | jq .payload
{% endraw %}{% endhighlight %}

### See also

* [maton trigger event](/manual/maton/trigger/event)
