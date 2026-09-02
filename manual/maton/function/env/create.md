---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function env create

```
maton function env create [<key>] --function <function-id> --value <value> [flags]
```

Set environment variables that are not set yet.

The call fails with a 409 if any key already exists, and nothing is written —
a whole `--env-file` lands or none of it does. Use
`maton function env update` to change a key that is already set.

`--type` defaults to `SENSITIVE`, matching what a key would land as
through `env update`. A `SENSITIVE` value is write-only, so `env list` will
only ever show it as (hidden); pass `--type PLAIN` for one you can read back.
It applies to every key in an `--env-file`, which has no way to say otherwise.

One key's value comes from `--value`, or is prompted for, or is read from
standard input when the command is not interactive. The prompt for a
`SENSITIVE` value does not echo. A value of `@path` reads the file at that
path, and `@-` reads stdin, matching the convention `maton api -F` uses.

`--env-file` instead reads a batch of keys from a dotenv-formatted file, or
from standard input when it is `-`. It takes no `<key>` and no `--value`.


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
	<dd>Whether the value is readable back (SENSITIVE when omitted): {PLAIN|SENSITIVE}</dd>

	<dt>
		<code>--value &lt;string&gt;</code></dt>
	<dd>Value, prompted for or read from standard input when omitted</dd>
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
$ maton function env create GREETING -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --value hi --type PLAIN
$ maton function env create TOKEN -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function env create KEY -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --value @key.pem
$ maton function env create -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --env-file .env
$ cat .env | maton function env create -f 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01 --env-file -
{% endraw %}{% endhighlight %}

### See also

* [maton function env](/manual/maton/function/env)
