---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton login

```
maton login [flags]
```

Login to your Maton account to set up the CLI.

Prints a login link and exits 8 to say the sign-in is pending. Sign in on
this or any other device, and the page shows a verification code.
Finish with maton login --code <CODE>. The login link works for up to 30
minutes. The CLI then stores a short-lived access token that it renews
automatically, so no long-lived key is kept on the machine.


### Available commands

* [maton login list](/manual/maton/login/list)
* [maton login switch](/manual/maton/login/switch)


### Options


<dl class="flags">
	<dt>
		<code>--api-key</code></dt>
	<dd>Paste in a Maton API key instead of signing in with a verification code</dd>

	<dt>
		<code>--code &lt;string&gt;</code></dt>
	<dd>Finish a pending sign-in with the verification code shown in the browser</dd>

	<dt>
		<code>--insecure-storage</code></dt>
	<dd>Save credentials in plain text instead of the OS keyring</dd>
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
# Print a login link and open it in the browser
$ maton login

# Finish a sign-in started by an earlier run
$ maton login --code K7QX3MZP

# Open the Maton login page and paste in an API key
$ maton login --api-key
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
