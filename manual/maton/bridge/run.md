---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton bridge run

```
maton bridge run [<bridge-id>] [flags]
```

Run a bridge in the foreground until you press Ctrl+C or close the process. The first run registers a bridge named after this computer and reuses it on later runs. Pass a bridge ID to run an existing bridge here instead. An API key saved by 'maton bridge install' is used over the active profile unless --profile or MATON_API_KEY is set.

### Options


<dl class="flags">
	<dt>
		<code>--url &lt;string&gt;</code></dt>
	<dd>Bridge socket base URL; the bridge ID is appended (default: derived from the API URL, or MATON_BRIDGE_URL)</dd>
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
$ maton bridge run
$ maton bridge run 3f2b9c1e-5d4a-4e8b-9a7c-1b2d3e4f5a6b
{% endraw %}{% endhighlight %}

### See also

* [maton bridge](/manual/maton/bridge)
