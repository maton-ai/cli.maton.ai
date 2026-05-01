---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton asana project create

Create a new project

```
maton asana project create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--color &lt;string&gt;</code></dt>
	<dd>Project color (e.g. light-green, dark-pink)</dd>

	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--due-on &lt;string&gt;</code></dt>
	<dd>Due date (YYYY-MM-DD)</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>Project name (required)</dd>

	<dt>
		<code>--notes &lt;string&gt;</code></dt>
	<dd>Project description</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-w</code>, 
		<code>--workspace &lt;string&gt;</code></dt>
	<dd>Workspace gid (required)</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton asana project create --workspace 12345 --name 'Q3 Roadmap'
$ maton asana project create -w 12345 --name 'Launch' --due-on 2026-09-30 --color light-green
{% endraw %}{% endhighlight %}

### See also

* [maton asana project](/manual/maton/asana/project)
