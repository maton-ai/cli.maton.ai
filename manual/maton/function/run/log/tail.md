---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function run log tail

```
maton function run log tail --function <function-id> [flags]
```

Print a run's log events as they land, and keep polling until the run has
ended and two consecutive polls return nothing new — or until `--timeout`
elapses, or Ctrl-C. A run's logs are bounded by the execution limit, so this
terminates on its own; there is no checkpoint to resume from.

The end of the run is read from the run's own `ended_at`, not from the
terminal `REPORT RunId:` line: a `--filter-pattern` that does not match
`REPORT` would otherwise never let the tail finish.

A failed poll is logged and retried rather than ending the tail, since
logs are eventually consistent and a blip mid-run should not throw away a
follow that is otherwise working. `--exit-status` makes the first one
fatal instead, for scripts that would rather fail than print a partial run.

There is no `--until`, which would contradict following. `--since` takes
an RFC3339 timestamp or a duration such as `10m`. Output is not paged.


### Options


<dl class="flags">
	<dt>
		<code>--exit-status</code></dt>
	<dd>Exit non-zero on a poll error instead of logging and continuing</dd>

	<dt>
		<code>--filter-pattern &lt;string&gt;</code></dt>
	<dd>CloudWatch filter pattern</dd>

	<dt><code>-f</code>, 
		<code>--function &lt;string&gt;</code></dt>
	<dd>Function ID this resource belongs to (required)</dd>

	<dt>
		<code>--interval &lt;duration&gt; (default &#34;2s&#34;)</code></dt>
	<dd>Polling interval</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-r</code>, 
		<code>--run &lt;string&gt;</code></dt>
	<dd>Run to read (the newest run when omitted)</dd>

	<dt>
		<code>--since &lt;string&gt;</code></dt>
	<dd>Start of the window: RFC3339 or a duration like 10m</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--timeout &lt;duration&gt; (default &#34;1m30s&#34;)</code></dt>
	<dd>Give up following after this long</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton function run logs follow,  maton function runs log follow,  maton function runs logs follow,  maton functions run log follow,  maton functions run logs follow,  maton functions runs log follow,  maton functions runs logs follow, maton function run log follow

### JSON Fields

`message`, `timestamp`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# Follow the newest run
$ maton function run log tail --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01

# Follow one run, streaming NDJSON into jq
$ maton function run log tail -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --run run_abc123 --json timestamp,message
{% endraw %}{% endhighlight %}

### See also

* [maton function run log](/manual/maton/function/run/log)
