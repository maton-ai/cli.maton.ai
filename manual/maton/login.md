---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton login

```
maton login [flags]
```

Login to your Maton account to set up the CLI. By default, this signs you in through your browser and stores a short-lived access token that the CLI renews automatically, so no long-lived key is kept on the machine. Use --device to earn that same token on a host with no browser: the CLI prints a one-time code that you approve from any other device. The default flow falls back to it by itself when no browser can be opened. Use --api-key to paste in a Maton API key instead: the CLI opens the Maton login page, and you copy the key back into the terminal. --api-key, --oauth, and --device cannot be combined; pick the one that matches the host. Add --interactive to any of these when you don't want a browser launched at all: the CLI prints the URL to open yourself, or just prompts for an API key.

### Available commands

* [maton login list](/manual/maton/login/list)
* [maton login switch](/manual/maton/login/switch)


### Options


<dl class="flags">
	<dt>
		<code>--api-key</code></dt>
	<dd>Paste in a Maton API key instead of signing in through the browser</dd>

	<dt>
		<code>--device</code></dt>
	<dd>Sign in with a one-time code shown in the terminal; no local browser needed</dd>

	<dt>
		<code>--insecure-storage</code></dt>
	<dd>Save credentials in plain text instead of the OS keyring</dd>

	<dt><code>-i</code>, 
		<code>--interactive</code></dt>
	<dd>Skip launching a browser; on its own, prompt for an API key</dd>

	<dt>
		<code>--oauth</code></dt>
	<dd>Sign in through the browser and store a renewable token (the default)</dd>
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
# Sign in with your browser; no API key to copy
$ maton login

# Sign in from a container or an SSH session with a one-time code
$ maton login --device

# Open the Maton login page and paste in an API key
$ maton login --api-key
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
