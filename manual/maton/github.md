---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github

Manage repos, issues, and pull requests in GitHub.

### Available commands

* [maton github issue](/manual/maton/github/issue)
* [maton github label](/manual/maton/github/label)
* [maton github pr](/manual/maton/github/pr)
* [maton github release](/manual/maton/github/release)
* [maton github repo](/manual/maton/github/repo)
* [maton github whoami](/manual/maton/github/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton github whoami
$ maton github repo view --repo maton-ai/cli
$ maton github issue list --repo maton-ai/cli --state open
$ maton github pr view --repo maton-ai/cli 1
$ maton github label list --repo maton-ai/cli
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
