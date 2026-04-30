---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton upgrade

```
maton upgrade [version] [flags]
```

Upgrade the maton CLI by re-running the installer for the active install
method:

  - npm-managed:  `npm install -g @maton/cli`
  - bun-managed:  `bun add -g @maton/cli`
  - Windows:      `irm https://maton.ai/install.ps1 | iex`
  - otherwise:    `curl -fsSL https://maton.ai/install.sh | bash`

Pass a version (e.g. "1.2.3") to pin.


### Options


<dl class="flags">
	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the command that would run without executing it</dd>

	<dt>
		<code>--force</code></dt>
	<dd>Re-run the installer even if already on the requested version</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton update

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton upgrade
$ maton upgrade 1.2.3
$ maton upgrade --dry-run
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
