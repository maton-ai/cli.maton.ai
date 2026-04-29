---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github

Manage repos, issues, and pull requests in GitHub.

### Available commands

* [maton github issue](./maton_github_issue)
* [maton github label](./maton_github_label)
* [maton github pr](./maton_github_pr)
* [maton github release](./maton_github_release)
* [maton github repo](./maton_github_repo)
* [maton github whoami](./maton_github_whoami)


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

* [maton](./maton)
