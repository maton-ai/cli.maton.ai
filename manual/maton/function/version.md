---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function version

Every code change to a function creates a new version. There is no activate
or deploy step: roll back by pointing the function at an older version with
`maton function update <function-id> --version <n>`.


### Available commands

* [maton function version get](/manual/maton/function/version/get)
* [maton function version list](/manual/maton/function/version/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton functions versions, maton function versions

{% endraw %}
### See also

* [maton function](/manual/maton/function)
