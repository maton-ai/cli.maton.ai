---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function run

Every invocation of a function records a run: the request it received, the
response it produced, and the log events it wrote.

Runs are recorded, not started, here. To invoke a function, point
`maton api` at its URL.

The logs belong to a run rather than to the function, so they live under
this command: `maton function run log list` and `… log tail`.


### Available commands

* [maton function run get](/manual/maton/function/run/get)
* [maton function run list](/manual/maton/function/run/list)
* [maton function run log](/manual/maton/function/run/log)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton functions runs, maton function runs

{% endraw %}
### See also

* [maton function](/manual/maton/function)
