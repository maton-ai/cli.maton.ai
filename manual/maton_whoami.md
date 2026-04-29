---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton whoami

```
maton whoami [flags]
```

Display the current authentication state for the Maton CLI. Calls the Maton /user endpoint to verify the stored API key and fetch account info. Use --format json for output suitable for scripting or agent consumption. Exit codes: 0  Authenticated 1  Not authenticated, or an error occurred

### Options


<dl class="flags">
	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; for a stable JSON schema (suitable for scripting)</dd>
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
$ maton whoami
$ maton whoami --format json
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
