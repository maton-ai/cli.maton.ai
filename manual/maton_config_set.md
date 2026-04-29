---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton config set

Update configuration with a value for the given key

```
maton config set <key> <value> [flags]
```

### Options


<dl class="flags">
	<dt><code>-h</code>, 
		<code>--host &lt;string&gt;</code></dt>
	<dd>Set per-host setting</dd>
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
$ maton config set editor vim
$ maton config set editor "code --wait"
$ maton config set git_protocol ssh --host github.com
$ maton config set prompt disabled
{% endraw %}{% endhighlight %}

### See also

* [maton config](./maton_config)
