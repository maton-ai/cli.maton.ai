---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton config get

Print the value of a given configuration key

```
maton config get <key> [flags]
```

### Options


<dl class="flags">
	<dt><code>-h</code>, 
		<code>--host &lt;string&gt;</code></dt>
	<dd>Get per-host setting</dd>
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
$ maton config get git_protocol
{% endraw %}{% endhighlight %}

### See also

* [maton config](./maton_config)
