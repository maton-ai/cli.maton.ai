---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr

Create, get, list, and manage pull requests

### Available commands

* [maton github pr checks](/manual/maton/github/pr/checks)
* [maton github pr close](/manual/maton/github/pr/close)
* [maton github pr comment](/manual/maton/github/pr/comment)
* [maton github pr create](/manual/maton/github/pr/create)
* [maton github pr diff](/manual/maton/github/pr/diff)
* [maton github pr edit](/manual/maton/github/pr/edit)
* [maton github pr get](/manual/maton/github/pr/get)
* [maton github pr list](/manual/maton/github/pr/list)
* [maton github pr merge](/manual/maton/github/pr/merge)
* [maton github pr ready](/manual/maton/github/pr/ready)
* [maton github pr reopen](/manual/maton/github/pr/reopen)
* [maton github pr review](/manual/maton/github/pr/review)
* [maton github pr search](/manual/maton/github/pr/search)
* [maton github pr status](/manual/maton/github/pr/status)
* [maton github pr update-branch](/manual/maton/github/pr/update-branch)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton github pull-request, maton github prs

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github pr list --repo maton-ai/cli --state open
$ maton github pr get 123 --repo maton-ai/cli
$ maton github pr create --repo maton-ai/cli --base main --head feature --title "New thing"
$ maton github pr merge 123 --repo maton-ai/cli --squash
{% endraw %}{% endhighlight %}

### See also

* [maton github](/manual/maton/github)
