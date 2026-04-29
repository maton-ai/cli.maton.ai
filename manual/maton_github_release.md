---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github release

Manage GitHub releases and their assets

### Available commands

* [maton github release create](./maton_github_release_create)
* [maton github release delete](./maton_github_release_delete)
* [maton github release delete-asset](./maton_github_release_delete-asset)
* [maton github release download](./maton_github_release_download)
* [maton github release edit](./maton_github_release_edit)
* [maton github release list](./maton_github_release_list)
* [maton github release upload](./maton_github_release_upload)
* [maton github release view](./maton_github_release_view)


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
$ maton github release view v1.0.0 --repo maton-ai/cli
$ maton github release create v1.0.0 --repo maton-ai/cli --title "v1.0.0" --notes "..."
$ maton github release delete v1.0.0 --repo maton-ai/cli --yes
{% endraw %}{% endhighlight %}

### See also

* [maton github](./maton_github)
