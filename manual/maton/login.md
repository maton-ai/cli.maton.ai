---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton login

```
maton login [flags]
```

Login to your Maton account to set up the CLI. By default, the CLI prints a user code and a link, then exits 8 to say the sign-in is pending; open the link on this or any other device, approve the code, then run maton login again. That run exits 0 once the code is approved, exits 8 and shows the code again while it is still pending, and exits 1 if it was denied. A code that expired is replaced with a new one, and the run exits 8. Exit 0 always means you are signed in. The CLI then stores a short-lived access token that the CLI renews automatically, so no long-lived key is kept on the machine. This works the same on a desktop, over SSH, or in a container. Use --api-key to paste in a Maton API key instead: the CLI opens the Maton login page, and you copy the key back into the terminal. --api-key and --device cannot be combined; pick the one that matches the host.

### Available commands

* [maton login list](/manual/maton/login/list)
* [maton login switch](/manual/maton/login/switch)


### Options


<dl class="flags">
	<dt>
		<code>--api-key</code></dt>
	<dd>Paste in a Maton API key instead of signing in with device authorization</dd>

	<dt>
		<code>--device</code></dt>
	<dd>Sign in with device authorization, using a user code shown in the terminal (the default)</dd>

	<dt>
		<code>--insecure-storage</code></dt>
	<dd>Save credentials in plain text instead of the OS keyring</dd>

	<dt><code>-i</code>, 
		<code>--interactive</code></dt>
	<dd>Skip launching a browser for --oauth or --api-key; on its own, prompt for an API key</dd>

	<dt>
		<code>--oauth</code></dt>
	<dd>Sign in through a browser that redirects back to this host</dd>
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
# Sign in with device authorization
$ maton login

# Open the Maton login page and paste in an API key
$ maton login --api-key
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
