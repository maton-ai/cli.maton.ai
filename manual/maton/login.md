---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton login

```
maton login [flags]
```

Login to your Maton account to set up the CLI. By default, this opens your browser to the Maton login page. After signing in, copy your API key and paste it back into the terminal. Use --interactive when you don't want to launch a browser (for example, on a headless host). Use --oauth to sign in with your browser instead of an API key: the CLI then holds a short-lived access token that it renews automatically, so no long-lived key is stored on the machine.

### Available commands

* [maton login list](/manual/maton/login/list)
* [maton login switch](/manual/maton/login/switch)


### Options


<dl class="flags">
	<dt>
		<code>--insecure-storage</code></dt>
	<dd>Save the API key in plain text instead of the OS keyring</dd>

	<dt><code>-i</code>, 
		<code>--interactive</code></dt>
	<dd>Skip launching the browser; only prompt for an API key</dd>

	<dt>
		<code>--oauth</code></dt>
	<dd>Sign in through the browser and store a renewable token instead of an API key</dd>
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
# Open the Maton login page and paste in an API key
$ maton login

# Skip the browser launch and just paste an API key
$ maton login --interactive

# Sign in with your browser; no API key to copy
$ maton login --oauth
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
