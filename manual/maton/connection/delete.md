---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton connection delete

```
maton connection delete <id> [flags]
```

Delete an app connection by its ID. Use --yes to skip the confirmation prompt (required when running non-interactively).

### Options


<dl class="flags">
	<dt>
		<code>--yes</code></dt>
	<dd>Skip confirmation prompt</dd>
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
$ maton connection delete conn_abc123
$ maton connection delete conn_abc123 --yes
{% endraw %}{% endhighlight %}

### See also

* [maton connection](/manual/maton/connection)
