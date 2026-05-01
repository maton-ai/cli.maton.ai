---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github label

Create, list, edit, and delete labels in a repository

### Available commands

* [maton github label clone](/manual/maton/github/label/clone)
* [maton github label create](/manual/maton/github/label/create)
* [maton github label delete](/manual/maton/github/label/delete)
* [maton github label edit](/manual/maton/github/label/edit)
* [maton github label list](/manual/maton/github/label/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton github labels

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github label list --repo maton-ai/cli
$ maton github label create bug --repo maton-ai/cli --color d73a4a
$ maton github label edit bug --repo maton-ai/cli --description "Something is broken"
$ maton github label delete bug --repo maton-ai/cli --yes
{% endraw %}{% endhighlight %}

### See also

* [maton github](/manual/maton/github)
