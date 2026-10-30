---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton bridge install

```
maton bridge install [<bridge-id>] [flags]
```

Start a bridge whenever you log in to this computer (LaunchAgent on macOS, systemd user unit on Linux, Task Scheduler on Windows). It runs as you, restarts on failure, and uses the current profile. If MATON_API_KEY is set, that key is saved for the bridge instead, in the keyring when available. Saving it asks for confirmation; use --yes to skip it (required when running non-interactively). Pass a bridge ID to run an existing bridge instead of this computer's saved one. To replace an installed bridge, run 'maton bridge uninstall' first.

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
$ maton bridge install
{% endraw %}{% endhighlight %}

### See also

* [maton bridge](/manual/maton/bridge)
