---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton token

```
maton token
```

Print a valid access token for the active profile, renewing it first if it
has expired. Only profiles signed in with 'maton login --oauth' have a
renewable token; for API-key profiles this exits non-zero, since printing a
long-lived key on request is not the same operation.

Intended for programs that need to call the Maton API directly:

    curl -H "Authorization: Bearer $(maton token)" https://api.maton.ai/user

The token is short-lived, so fetch it per invocation rather than caching it.


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton token
$ curl -H "Authorization: Bearer $(maton token)" https://api.maton.ai/user
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
