---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function create

```
maton function create --name <name> (--dir <dir> | --file <file>) [flags]
```

Create a function from a local source tree and print the URL it answers on.

Most of the time you want `maton function deploy` instead: it creates the
function the same way, then remembers it, so subsequent deploys of the same
directory need no function ID. This command is the raw POST — it creates a new
function every time it runs and records nothing locally, which is what a script
usually wants.

`--dir` walks a directory. Dot-prefixed files and directories are always
skipped, because the service rejects dot-prefixed path segments outright, so
uploading them could only ever fail. A default ignore list covers
`node_modules`, `__pycache__`, `venv`, `env`, `site-packages`, `dist`,
`build`, `target`, and `vendor`; add to it with `--ignore` or turn it off
with `--no-default-ignore`. Functions carry text files only, so a non-UTF-8
or NUL-containing file is skipped inside `--dir` and an error when named by
`--file`.

`--file <local>[:<remote>]` adds or overrides one path after `--dir` has been
walked. `--file -:main.py` reads stdin.

The handler names the function the runtime calls, as `<module>.<symbol>` —
`main.handler` is `handler` in `main.py`, and `lib/util.handler` is
`handler` in `lib/util.py`. The module carries no extension, because the
runtime supplies it. It is called as `handler(event, context)`; see
`maton function --help` for the event.

The handler and runtime are inferred when they can be: `main.py` implies
`main.handler` on `python3.12`, and `index.js` implies
`index.handler` on `nodejs22.x`. When the tree is ambiguous the command
fails locally and names the candidates.

Use `--dry-run` to print the manifest without uploading. Environment
variables are set separately with `maton function env create`.

The URL is a wildcard-DNS subdomain and takes a moment to start resolving, so
an invocation immediately after create can fail before the name propagates.


### Options


<dl class="flags">
	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description</dd>

	<dt><code>-D</code>, 
		<code>--dir &lt;string&gt;</code></dt>
	<dd>Directory to upload</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the bundle manifest and exit without uploading</dd>

	<dt>
		<code>--file &lt;local[:remote]&gt;</code></dt>
	<dd>File to upload as local[:remote] (repeatable)</dd>

	<dt>
		<code>--handler &lt;&lt;module&gt;.&lt;symbol&gt;&gt;</code></dt>
	<dd>Handler as &lt;module&gt;.&lt;symbol&gt; (inferred when omitted)</dd>

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
	<dd>Function name, which seeds the URL label (required)</dd>

	<dt>
		<code>--network-policy &lt;string&gt;</code></dt>
	<dd>Whether the sandbox may reach the network: {ALLOW_ALL|DENY_ALL}</dd>

	<dt>
		<code>--no-default-ignore</code></dt>
	<dd>Do not apply the default ignore list</dd>

	<dt>
		<code>--runtime &lt;string&gt;</code></dt>
	<dd>Runtime (inferred from the handler&#39;s file when omitted): {python3.12|nodejs22.x}</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

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
# Create from a directory, inferring main.handler and python3.12
$ maton function create --name my-fn --dir ./my-fn

# See what would be uploaded first
$ maton function create --name my-fn --dir . --dry-run

# Create from a single file on stdin
$ cat handler.py | maton function create --name my-fn --file -:main.py

# Point at a different symbol
$ maton function create --name my-fn --dir ./my-fn --handler main.webhook

# Node function, public
$ maton function create --name my-fn --dir ./my-fn --runtime nodejs22.x --visibility PUBLIC
{% endraw %}{% endhighlight %}

### See also

* [maton function](/manual/maton/function)
