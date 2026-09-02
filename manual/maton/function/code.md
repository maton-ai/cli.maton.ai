---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function code

Read the source bundle behind a function version.

The route answers with a presigned URL rather than the bundle itself, and the
two commands here split along that seam: `get` returns the envelope, and
`download` follows it and writes the tree.


### Available commands

* [maton function code download](/manual/maton/function/code/download)
* [maton function code get](/manual/maton/function/code/get)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### See also

* [maton function](/manual/maton/function)
