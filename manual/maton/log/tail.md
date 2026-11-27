---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton log tail

```
maton log tail [flags]
```

Print each new log in your account as it arrives, starting from now, until
interrupted with Ctrl-C.

`--since` starts further back: it takes an RFC3339 timestamp or a duration
such as `10m` or `7d`, meaning that long ago. Every log since then
is printed before the tail catches up, so a long `--since` can print a
large backlog first. Logs are kept for 30 days. Output is not paged.
With `--json` the stream is newline-delimited JSON, one object per line.

Each poll rereads one minute before the newest log seen to catch entries
that arrive out of order. Increase `--overlap` if entries can arrive further
behind. Older logs outside that window require a separate `maton log list`.

A failed poll is reported and retried rather than ending the tail.
`--exit-status` makes the first one fatal instead.

See `maton log --help` for the `--search` query syntax.


### Options


<dl class="flags">
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
		<code>--level &lt;string&gt;</code></dt>
	<dd>Filter by level: {info|warning|error}</dd>

	<dt>
		<code>--overlap &lt;duration&gt; (default &#34;1m0s&#34;)</code></dt>
	<dd>How far behind the newest log to look for late arrivals</dd>

	<dt>
		<code>--request-id &lt;string&gt;</code></dt>
	<dd>Filter by the request that wrote the log</dd>

	<dt><code>-S</code>, 
		<code>--search &lt;string&gt;</code></dt>
	<dd>Filter with a search query</dd>

	<dt>
		<code>--since &lt;string&gt;</code></dt>
	<dd>Where to start: RFC3339 or a duration like 10m or 7d (default now)</dd>

	<dt>
		<code>--source &lt;string&gt;</code></dt>
	<dd>Filter by source, such as gateway or function</dd>

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

 maton logs follow, maton log follow

### JSON Fields

`level`, `log_id`, `message`, `request_id`, `source`, `timestamp`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# Follow everything
$ maton log tail

# Follow errors, starting ten minutes back
$ maton log tail --level error --since 10m

# Follow function logs, streaming NDJSON into jq
$ maton log tail --source function --json timestamp,message | jq -r .message
{% endraw %}{% endhighlight %}

### See also

* [maton log](/manual/maton/log)
