---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github release

Manage GitHub releases and their assets

### Available commands

* [maton github release create](/manual/maton/github/release/create)
* [maton github release delete](/manual/maton/github/release/delete)
* [maton github release delete-asset](/manual/maton/github/release/delete-asset)
* [maton github release download](/manual/maton/github/release/download)
* [maton github release edit](/manual/maton/github/release/edit)
* [maton github release get](/manual/maton/github/release/get)
* [maton github release list](/manual/maton/github/release/list)
* [maton github release upload](/manual/maton/github/release/upload)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton github releases

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github release list --repo maton-ai/cli
$ maton github release get v1.0.0 --repo maton-ai/cli
$ maton github release create v1.0.0 --repo maton-ai/cli --title "v1.0.0" --notes "..."
$ maton github release delete v1.0.0 --repo maton-ai/cli --yes
{% endraw %}{% endhighlight %}

### See also

* [maton github](/manual/maton/github)
