---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton completion

```
maton completion -s <shell>
```

Generate shell completion scripts for Maton CLI commands.

When installing Maton CLI through a package manager, it's possible that
no additional shell configuration is necessary to gain completion support. For
Homebrew, see <https://docs.brew.sh/Shell-Completion>

If you need to set up completions manually, follow the instructions below. The exact
config file locations might vary based on your system. Make sure to restart your
shell before testing whether completions are working.

### bash

First, ensure that you install `bash-completion` using your package manager.

After, add this to your `~/.bash_profile`:

	eval "$(maton completion -s bash)"

### zsh

Generate a `_maton` completion script and put it somewhere in your `$fpath`:

	maton completion -s zsh > /usr/local/share/zsh/site-functions/_maton

Ensure that the following is present in your `~/.zshrc`:

	autoload -U compinit
	compinit -i

Zsh version 5.7 or later is recommended.

### fish

Generate a `maton.fish` completion script:

	maton completion -s fish > ~/.config/fish/completions/maton.fish

### PowerShell

Open your profile script with:

	mkdir -Path (Split-Path -Parent $profile) -ErrorAction SilentlyContinue
	notepad $profile

Add the line and save the file:

	Invoke-Expression -Command $(maton completion -s powershell | Out-String)


### Options


<dl class="flags">
	<dt><code>-s</code>, 
		<code>--shell &lt;string&gt;</code></dt>
	<dd>Shell type: {bash|zsh|fish|powershell}</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### See also

* [maton](./maton)
