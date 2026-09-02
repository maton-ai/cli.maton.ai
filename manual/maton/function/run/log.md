---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function run log

Read the log events a run wrote to stdout and stderr. `list` returns what
is there now; `tail` follows a live run until it finishes.

Logs belong to a run, so both take `--run`. With it omitted the function's
newest run is used, which is almost always the one you just triggered —
though an invocation answers with its own run ID in `X-Function-Run-Id`,
so `maton api <url> -i` names the run exactly rather than relying on that
default.

Logs are eventually consistent, and the server intersects your window with
the run's own start and end times plus a five-second margin. A run that
finished a moment ago will often show zero events; try again.

The lines are Lambda-shaped, which is what makes `--filter-pattern` worth
reaching for. A run brackets its output with `START RunId: <run-id>`
and `END RunId: <run-id>`, then a `REPORT RunId: <run-id>` line
carrying the duration. A handler that raises logs its traceback followed by
`[ERROR] Runtime.ExitError`; one that runs past the execution limit logs
`<run-id> Task timed out after <n> seconds`; an entrypoint that fails to
load logs `[ERROR] Runtime.InvalidEntrypoint`.


### Available commands

* [maton function run log list](/manual/maton/function/run/log/list)
* [maton function run log tail](/manual/maton/function/run/log/tail)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton function runs logs,  maton functions run logs,  maton functions runs logs, maton function run logs

{% endraw %}
### See also

* [maton function run](/manual/maton/function/run)
