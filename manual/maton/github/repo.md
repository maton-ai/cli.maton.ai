---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github repo

Create, get, list, and manage repositories

### Available commands

* [maton github repo archive](/manual/maton/github/repo/archive)
* [maton github repo create](/manual/maton/github/repo/create)
* [maton github repo credits](/manual/maton/github/repo/credits)
* [maton github repo delete](/manual/maton/github/repo/delete)
* [maton github repo edit](/manual/maton/github/repo/edit)
* [maton github repo get](/manual/maton/github/repo/get)
* [maton github repo gitignore](/manual/maton/github/repo/gitignore)
* [maton github repo license](/manual/maton/github/repo/license)
* [maton github repo list](/manual/maton/github/repo/list)
* [maton github repo rename](/manual/maton/github/repo/rename)
* [maton github repo search](/manual/maton/github/repo/search)
* [maton github repo set-default](/manual/maton/github/repo/set-default)
* [maton github repo unarchive](/manual/maton/github/repo/unarchive)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton github repos, maton github repository

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github repo get --repo maton-ai/cli
$ maton github repo list --owner maton-ai
$ maton github repo create my-app --private
$ maton github repo delete --repo me/old-thing --yes
{% endraw %}{% endhighlight %}

### See also

* [maton github](/manual/maton/github)
