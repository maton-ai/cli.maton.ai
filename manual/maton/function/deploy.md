---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function deploy

```
maton function deploy [--dir <dir>] [flags]
```

Push a local source tree to Maton. The first run creates the function; every
run after that publishes a new version of the same one.

Which of the two happens is decided by a link file, `.maton/state.json`,
written into the deployed directory on the first successful create. It records
the function ID, so no function ID ever has to be typed and no name is ever
matched against the server. Deploy resolves its target in this order:

    1. --function <id>
    2. MATON_FUNCTION_ID
    3. .maton/state.json
    4. nothing linked, so create a new function

The link file is dot-prefixed, which means the bundler already skips it and it
can never be uploaded. It is per-account, so it should not be committed —
deploy prints a reminder rather than editing your `.gitignore` for you.

Two flags are create-only and are refused against a linked function. `--name`
is refused because renaming reallocates the URL, which is a deliberate act that
belongs to `maton function update --name`; `--runtime` is refused because a
function's runtime is immutable. When creating, the name defaults to the
directory's own name, slugified.

Bundling, inference, and the ignore rules are the same as `create`; see that
command for the details. `--dry-run` resolves the target and prints both it and
the full manifest without uploading anything.

`create` and `update` remain available and map one-to-one onto POST and
PATCH, which is what you want from a script. For deploying code by hand, prefer
this command.


### Options


<dl class="flags">
	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description</dd>

	<dt><code>-D</code>, 
		<code>--dir &lt;string&gt; (default &#34;.&#34;)</code></dt>
	<dd>Directory to deploy</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the target and bundle manifest, then exit without uploading</dd>

	<dt>
		<code>--file &lt;local[:remote]&gt;</code></dt>
	<dd>Extra file to include as local[:remote] (repeatable)</dd>

	<dt>
		<code>--function &lt;string&gt;</code></dt>
	<dd>Deploy to this function ID, overriding any link</dd>

	<dt>
		<code>--handler &lt;&lt;module&gt;.&lt;symbol&gt;&gt;</code></dt>
	<dd>Handler as &lt;module&gt;.&lt;symbol&gt; (inferred on create, unchanged otherwise)</dd>

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
	<dd>Name for a new function (defaults to the directory name)</dd>

	<dt>
		<code>--network-policy &lt;string&gt;</code></dt>
	<dd>Whether the sandbox may reach the network: {ALLOW_ALL|DENY_ALL}</dd>

	<dt>
		<code>--no-default-ignore</code></dt>
	<dd>Do not apply the default ignore list</dd>

	<dt>
		<code>--runtime &lt;string&gt;</code></dt>
	<dd>Runtime for a new function (inferred when omitted): {python3.12|nodejs22.x}</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--visibility &lt;string&gt;</code></dt>
	<dd>Who can see the function: {PRIVATE|PUBLIC|UNLISTED}</dd>

	<dt>
		<code>--yes</code></dt>
	<dd>Create without confirmation (required when not running interactively)</dd>
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
# Create on the first run, publish a new version on every run after
$ cd my-fn && maton function deploy

# A directory somewhere else
$ maton function deploy --dir ./services/my-fn

# See the target and the manifest without uploading
$ maton function deploy --dry-run

# Adopt a function that already exists, then deploy to it from now on
$ maton function deploy --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01

# Non-interactive: create without the confirmation prompt
$ maton function deploy --yes --name my-fn

# Change a setting as part of the deploy
$ maton function deploy --visibility PUBLIC
{% endraw %}{% endhighlight %}

### See also

* [maton function](/manual/maton/function)
