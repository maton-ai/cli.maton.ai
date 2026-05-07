---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton salesforce composite

Wrap up to 25 Salesforce REST subrequests into one HTTP call.

  call   → POST /composite        sequential; subrequests can reference
                                  prior results via @{ref.field}
  batch  → POST /composite/batch  independent; each subrequest succeeds
                                  or fails on its own


### Available commands

* [maton salesforce composite batch](/manual/maton/salesforce/composite/batch)
* [maton salesforce composite call](/manual/maton/salesforce/composite/call)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### See also

* [maton salesforce](/manual/maton/salesforce)
