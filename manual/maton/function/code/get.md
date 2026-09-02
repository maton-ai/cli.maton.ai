---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function code get

```
maton function code get --function <function-id> [flags]
```

Show the presigned download envelope for a function version: the URL, the
bundle's SHA-256, and its size. One request, and nothing is written to disk.

The URL is valid for ten minutes and must be fetched *without* an
Authorization header — S3 rejects a bearer token sent alongside a presigned
signature. To skip both hazards, use `maton function code download`,
which follows the URL for you.


### Options


<dl class="flags">
	<dt><code>-f</code>, 
		<code>--function &lt;string&gt;</code></dt>
	<dd>Function ID this resource belongs to (required)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--version &lt;int&gt; (default 0)</code></dt>
	<dd>Version to describe (the current version when omitted)</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton functions code view, maton function code view

### JSON Fields

`download_url`, `sha256`, `size`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# The current version's envelope
$ maton function code get --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01

# An older version
$ maton function code get -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --version 2

# Just the URL, for scripting
$ maton function code get -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --jq .download_url
{% endraw %}{% endhighlight %}

### See also

* [maton function code](/manual/maton/function/code)
