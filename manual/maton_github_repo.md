---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github repo

Create, view, list, and manage repositories

### Available commands

* [maton github repo archive](./maton_github_repo_archive)
* [maton github repo create](./maton_github_repo_create)
* [maton github repo credits](./maton_github_repo_credits)
* [maton github repo delete](./maton_github_repo_delete)
* [maton github repo edit](./maton_github_repo_edit)
* [maton github repo gitignore](./maton_github_repo_gitignore)
* [maton github repo license](./maton_github_repo_license)
* [maton github repo list](./maton_github_repo_list)
* [maton github repo rename](./maton_github_repo_rename)
* [maton github repo search](./maton_github_repo_search)
* [maton github repo set-default](./maton_github_repo_set-default)
* [maton github repo unarchive](./maton_github_repo_unarchive)
* [maton github repo view](./maton_github_repo_view)


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
$ maton github repo view --repo maton-ai/cli
$ maton github repo list --owner maton-ai
$ maton github repo create my-app --private
$ maton github repo delete --repo me/old-thing --yes
{% endraw %}{% endhighlight %}

### See also

* [maton github](./maton_github)
