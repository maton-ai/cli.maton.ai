---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function update

```
maton function update <function-id> [flags]
```

Update a function. Only the flags you pass are changed.

For publishing code by hand, prefer `maton function deploy`: it takes no
function ID, having recorded one when it first created the function. Reach for
this command in scripts, where an explicit ID and a single PATCH are the point,
and for the two things deploy will not do — renaming, and rolling back.

Pass `--dir` or `--file` to publish new code, which creates a new version.
Roll back by pointing the function at an existing version with
`--version <n>`; there is no separate activate or deploy step, so
`--version` cannot be combined with new code.

A function's runtime is immutable, so there is no `--runtime` flag. Unlike
`create`, the handler is sent only when `--handler` is passed explicitly:
otherwise the server keeps the handler the current version already records.

`--handler` on its own publishes a new version. It is not a metadata edit
like `--name`: the handler belongs to a version, so changing it re-reads the
current version's files and publishes them again under the new handler. Nothing
is uploaded, and the code is unchanged, but the version number moves.

Renaming a function reallocates its URL. The old label is released
immediately, so the previous URL stops resolving for everyone holding it —
including any webhook configured elsewhere.


### Options


<dl class="flags">
	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>New description</dd>

	<dt><code>-D</code>, 
		<code>--dir &lt;string&gt;</code></dt>
	<dd>Directory to upload as a new version</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the bundle manifest and exit without uploading</dd>

	<dt>
		<code>--file &lt;local[:remote]&gt;</code></dt>
	<dd>File to upload as local[:remote] (repeatable)</dd>

	<dt>
		<code>--handler &lt;&lt;module&gt;.&lt;symbol&gt;&gt;</code></dt>
	<dd>Handler as &lt;module&gt;.&lt;symbol&gt;, which publishes a new version (unchanged when omitted)</dd>

	<dt>
		<code>--ignore &lt;stringArray&gt;</code></dt>
	<dd>Glob to exclude from --dir (repeatable)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>New name, which reallocates the URL</dd>

	<dt>
		<code>--network-policy &lt;string&gt;</code></dt>
	<dd>Whether the sandbox may reach the network: {ALLOW_ALL|DENY_ALL}</dd>

	<dt>
		<code>--no-default-ignore</code></dt>
	<dd>Do not apply the default ignore list</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--version &lt;int&gt; (default 0)</code></dt>
	<dd>Existing version to roll back to</dd>

	<dt>
		<code>--visibility &lt;string&gt;</code></dt>
	<dd>Who can see the function: {PRIVATE|PUBLIC|UNLISTED}</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### JSON Fields

`account_id`, `created_at`, `description`, `function_id`, `name`, `network_policy`, `runtime`, `star_count`, `updated_at`, `url`, `version`, `view_count`, `visibility`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# Publish new code
$ maton function update 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --dir ./my-fn

# Roll back to version 1
$ maton function update 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --version 1

# Point at a different symbol, publishing a new version of the same files
$ maton function update 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --handler main.webhook

# Make it public
$ maton function update 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --visibility PUBLIC
{% endraw %}{% endhighlight %}

### See also

* [maton function](/manual/maton/function)
