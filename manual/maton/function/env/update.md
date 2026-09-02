---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function env update

```
maton function env update [<key>] --function <function-id> --value <value> [flags]
```

Set environment variables, creating them when they do not exist yet. Unlike
`env create`, this does not mind a key that is already set, so it is the
idempotent way to change a value and the one to reach for when re-syncing an
`--env-file` you have edited.

`--type` changes the type when it is passed. Omitted, a key that already
exists keeps the type it has — but a key being created lands as
`SENSITIVE`, which is write-only, so `env list` will only ever show it as
(hidden). Pass `--type PLAIN` to create one you can read back. It applies to
every key in an `--env-file`, which has no way to say otherwise.

`--type` on its own changes only the type, keeping the value the key
already has. That is the one form that cannot create a key: there is no value
to create it with, so it fails if the key is not set yet.

Otherwise one key's value comes from `--value`, or is prompted for, or is
read from standard input when the command is not interactive. The prompt for
a `SENSITIVE` value does not echo. A value of `@path` reads the file at
that path, and `@-` reads stdin.

`--env-file` instead reads a batch of keys from a dotenv-formatted file, or
from standard input when it is `-`. It takes no `<key>` and no `--value`.
There is no batch endpoint for this, so the keys are written one at a time in
sorted order and a failure stops the run and reports which keys landed —
unlike `env create`, a batch here is not atomic.


### Options


<dl class="flags">
	<dt>
		<code>--env-file &lt;file&gt;</code></dt>
	<dd>Load a batch of keys and values from a dotenv-formatted file, or `-` for standard input</dd>

	<dt><code>-f</code>, 
		<code>--function &lt;string&gt;</code></dt>
	<dd>Function ID this resource belongs to (required)</dd>

	<dt>
		<code>--type &lt;string&gt;</code></dt>
	<dd>Whether the value is readable back (a new key is SENSITIVE when omitted): {PLAIN|SENSITIVE}</dd>

	<dt>
		<code>--value &lt;string&gt;</code></dt>
	<dd>New value, prompted for or read from standard input when omitted with no --type</dd>
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
$ maton function env update GREETING -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --value hello
$ maton function env update TOKEN -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function env update GREETING -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --type SENSITIVE
$ maton function env update -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --env-file .env
{% endraw %}{% endhighlight %}

### See also

* [maton function env](/manual/maton/function/env)
