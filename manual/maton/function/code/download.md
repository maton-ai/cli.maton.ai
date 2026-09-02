---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function code download

```
maton function code download --function <function-id> [flags]
```

Download the source bundle for a function version and write it to disk.

Two round trips: `code get` for the presigned URL, then the bundle
itself. By default the tree is exploded under `--dir`; pass `--output`
to save the raw bundle JSON instead (`--output -` writes it to stdout).

Existing files are never overwritten without `--clobber`.

There is no `--json` here: for this command it would have to mean "do not
download", which changes behavior rather than output format. `code get`
and `--output -` cover scripting.


### Options


<dl class="flags">
	<dt>
		<code>--clobber</code></dt>
	<dd>Overwrite existing files at the destination</dd>

	<dt><code>-D</code>, 
		<code>--dir &lt;string&gt; (default &#34;.&#34;)</code></dt>
	<dd>Directory to write the tree into</dd>

	<dt><code>-f</code>, 
		<code>--function &lt;string&gt;</code></dt>
	<dd>Function ID this resource belongs to (required)</dd>

	<dt><code>-o</code>, 
		<code>--output &lt;file&gt;</code></dt>
	<dd>Write the raw bundle JSON to a file (&#34;-&#34; for stdout)</dd>

	<dt>
		<code>--version &lt;int&gt; (default 0)</code></dt>
	<dd>Version to download (the current version when omitted)</dd>
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
# Explode the current version into ./pulled
$ maton function code download --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --dir ./pulled

# An older version
$ maton function code download -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --version 2 --dir ./v2

# The raw bundle JSON, for jq
$ maton function code download -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --output - | jq '.files | keys'
{% endraw %}{% endhighlight %}

### See also

* [maton function code](/manual/maton/function/code)
