---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear issue create

Create a new issue

```
maton linear issue create [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt><code>-d</code>, 
		<code>--description &lt;string&gt;</code></dt>
	<dd>Issue description (markdown)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--priority &lt;string&gt;</code></dt>
	<dd>Priority (0=None, 1=Urgent, 2=High, 3=Medium, 4=Low)</dd>

	<dt>
		<code>--team-id &lt;string&gt;</code></dt>
	<dd>Team ID (UUID, required)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt><code>-F</code>, 
		<code>--text-from-file &lt;file&gt;</code></dt>
	<dd>Read description from file (or `-` for stdin)</dd>

	<dt><code>-t</code>, 
		<code>--title &lt;string&gt;</code></dt>
	<dd>Issue title (required)</dd>
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
$ maton linear issue create --team-id <uuid> -t 'Fix login'
$ maton linear issue create --team-id <uuid> -t 'Bug' -d 'Repro: ...' --priority 2
$ cat description.md | maton linear issue create --team-id <uuid> -t 'Spec' -F -
{% endraw %}{% endhighlight %}

### See also

* [maton linear issue](/manual/maton/linear/issue)
