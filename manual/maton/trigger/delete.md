---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger delete

```
maton trigger delete <trigger-id> [flags]
```

Delete a trigger by its ID. Use --yes to skip the confirmation prompt (required when running non-interactively).

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
$ maton trigger delete trg_abc123
$ maton trigger delete trg_abc123 --yes
{% endraw %}{% endhighlight %}

### See also

* [maton trigger](/manual/maton/trigger)
