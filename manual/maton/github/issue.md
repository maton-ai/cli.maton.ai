---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue

Create, get, list, and edit issues

### Available commands

* [maton github issue close](/manual/maton/github/issue/close)
* [maton github issue comment](/manual/maton/github/issue/comment)
* [maton github issue create](/manual/maton/github/issue/create)
* [maton github issue delete](/manual/maton/github/issue/delete)
* [maton github issue develop](/manual/maton/github/issue/develop)
* [maton github issue edit](/manual/maton/github/issue/edit)
* [maton github issue get](/manual/maton/github/issue/get)
* [maton github issue list](/manual/maton/github/issue/list)
* [maton github issue lock](/manual/maton/github/issue/lock)
* [maton github issue pin](/manual/maton/github/issue/pin)
* [maton github issue reopen](/manual/maton/github/issue/reopen)
* [maton github issue search](/manual/maton/github/issue/search)
* [maton github issue status](/manual/maton/github/issue/status)
* [maton github issue transfer](/manual/maton/github/issue/transfer)
* [maton github issue unlock](/manual/maton/github/issue/unlock)
* [maton github issue unpin](/manual/maton/github/issue/unpin)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton github issues

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github issue list --repo maton-ai/cli --state open
$ maton github issue get 123 --repo maton-ai/cli
$ maton github issue create --repo maton-ai/cli --title "Bug" --body "..."
$ maton github issue close 123 --repo maton-ai/cli
{% endraw %}{% endhighlight %}

### See also

* [maton github](/manual/maton/github)
