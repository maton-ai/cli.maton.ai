---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton alias set

```
maton alias set <alias> <expansion> [flags]
```

Define a word that will expand to a full maton command when invoked.

The expansion may specify additional arguments and flags. If the expansion includes
positional placeholders such as `$1`, extra arguments that follow the alias will be
inserted appropriately. Otherwise, extra arguments will be appended to the expanded
command.

Use `-` as expansion argument to read the expansion string from standard input. This
is useful to avoid quoting issues when defining expansions.

If the expansion starts with `!` or if `--shell` was given, the expansion is a shell
expression that will be evaluated through the `sh` interpreter when the alias is
invoked. This allows for chaining multiple commands via piping and redirection.


### Options


<dl class="flags">
	<dt>
		<code>--clobber</code></dt>
	<dd>Overwrite existing aliases of the same name</dd>

	<dt><code>-s</code>, 
		<code>--shell</code></dt>
	<dd>Declare an alias to be passed through a shell interpreter</dd>
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
# Note: Command Prompt on Windows requires using double quotes for arguments
$ maton alias set pv 'pr view'
$ maton pv -w 123  #=> maton pr view -w 123

$ maton alias set bugs 'issue list --label=bugs'
$ maton bugs

$ maton alias set homework 'issue list --assignee @me'
$ maton homework

$ maton alias set 'issue mine' 'issue list --mention @me'
$ maton issue mine

$ maton alias set epicsBy 'issue list --author="$1" --label="epic"'
$ maton epicsBy vilmibm  #=> maton issue list --author="vilmibm" --label="epic"

$ maton alias set --shell igrep 'maton issue list --label="$1" | grep "$2"'
$ maton igrep epic foo  #=> maton issue list --label="epic" | grep "foo"
{% endraw %}{% endhighlight %}

### See also

* [maton alias](/manual/maton/alias)
