---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton log

Read the logs Maton records for your account. `list` returns what is there
now; `tail` follows new logs as they arrive.

Logs are kept for 30 days. Each one has a level (info, warning, or error),
a source, and, when it was written while serving an API request, that
request's ID.

`--search` takes a query. Bare words match the message, case-insensitively;
`level:`, `source:`, and `request_id:` match those fields. Terms combine with
AND, OR, NOT, and parentheses, and `*` and `?` are wildcards.


### Available commands

* [maton log list](/manual/maton/log/list)
* [maton log tail](/manual/maton/log/tail)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton logs

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton log list
$ maton log list --level error --since 1h
$ maton log list --search "timeout OR refused"
$ maton log tail --source gateway
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
