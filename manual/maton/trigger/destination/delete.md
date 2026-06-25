---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger destination delete

Remove a destination from a trigger

```
maton trigger destination delete <destination-id> --trigger <trigger-id> [flags]
```

### Options


<dl class="flags">
	<dt><code>-t</code>, 
		<code>--trigger &lt;string&gt;</code></dt>
	<dd>Trigger ID this resource belongs to (required)</dd>

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
$ maton trigger destination delete dst_123 --trigger trg_abc123
$ maton trigger destination delete dst_123 --trigger trg_abc123 --yes
{% endraw %}{% endhighlight %}

### See also

* [maton trigger destination](/manual/maton/trigger/destination)
