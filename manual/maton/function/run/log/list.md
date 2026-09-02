---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function run log list

```
maton function run log list --function <function-id> [flags]
```

List the log events one run has produced so far, oldest first.

`--since` and `--until` take an RFC3339 timestamp or a duration such as
`10m`, meaning that long ago. To watch a run that is still going instead
of taking a snapshot of it, use `maton function run log tail`.

See `maton function run log --help` for the shape of the lines, which is
what `--filter-pattern` matches against.


### Options


<dl class="flags">
	<dt>
		<code>--filter-pattern &lt;string&gt;</code></dt>
	<dd>CloudWatch filter pattern</dd>

	<dt><code>-f</code>, 
		<code>--function &lt;string&gt;</code></dt>
	<dd>Function ID this resource belongs to (required)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Maximum number of events to fetch (0 = no limit)</dd>

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
		<code>--until &lt;string&gt;</code></dt>
	<dd>End of the window: RFC3339 or a duration like 10m</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton function run logs ls,  maton function runs log ls,  maton function runs logs ls,  maton functions run log ls,  maton functions run logs ls,  maton functions runs log ls,  maton functions runs logs ls, maton function run log ls

### JSON Fields

`message`, `timestamp`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# The newest run's logs
$ maton function run log list --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01

# One specific run, last ten minutes
$ maton function run log list -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --run run_abc123 --since 10m

# Only errors, as NDJSON
$ maton function run log list -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --filter-pattern ERROR --json timestamp,message
{% endraw %}{% endhighlight %}

### See also

* [maton function run log](/manual/maton/function/run/log)
