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
$ maton alias set prv 'github pr get'
$ maton prv 123  #=> maton github pr get 123

$ maton alias set bugs 'github issue list --label=bug'
$ maton bugs

$ maton alias set standup 'slack message send --channel C0123456789 --text'
$ maton standup "What I did today..."

$ maton alias set 'slack ping' 'slack message send --channel C0123456789 --text "ping"'
$ maton slack ping

$ maton alias set authoredBy 'github issue list --author="$1" --label="bug"'
$ maton authoredBy octocat  #=> maton github issue list --author="octocat" --label="bug"

$ maton alias set --shell igrep 'maton github issue list --label="$1" | grep "$2"'
$ maton igrep bug foo  #=> maton github issue list --label="bug" | grep "foo"
{% endraw %}{% endhighlight %}

### See also

* [maton alias](/manual/maton/alias)
