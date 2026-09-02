---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function env

Manage the environment variables a function's sandbox sees.

`env create` and `env update` are different operations, not two spellings
of one. `env create` fails with a 409 if the key already exists, which is what
you want when seeding a new function. `env update` writes over a key that is
already set and creates one that is not, which is what you want when changing
a value — and it is the idempotent one.

A `SENSITIVE` value is write-only: it is never returned, so `env list`
shows it as (hidden).

The sandbox's environment is the variables from `function env` plus
`MATON_API_KEY`, which is runtime-provided.


### Available commands

* [maton function env create](/manual/maton/function/env/create)
* [maton function env delete](/manual/maton/function/env/delete)
* [maton function env list](/manual/maton/function/env/list)
* [maton function env update](/manual/maton/function/env/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### See also

* [maton function](/manual/maton/function)
