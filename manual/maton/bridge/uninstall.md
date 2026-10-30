---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton bridge uninstall

```
maton bridge uninstall
```

Stop the bridge on this computer, and remove it from your login services. The bridge stays registered under the same ID so 'maton bridge install' resumes it; run 'maton bridge delete <bridge-id>' to remove it from your account.

### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### See also

* [maton bridge](/manual/maton/bridge)
