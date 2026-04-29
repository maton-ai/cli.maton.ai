---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github pr

Create, view, list, and manage pull requests

### Available commands

* [maton github pr checks](./maton_github_pr_checks)
* [maton github pr close](./maton_github_pr_close)
* [maton github pr comment](./maton_github_pr_comment)
* [maton github pr create](./maton_github_pr_create)
* [maton github pr diff](./maton_github_pr_diff)
* [maton github pr edit](./maton_github_pr_edit)
* [maton github pr list](./maton_github_pr_list)
* [maton github pr merge](./maton_github_pr_merge)
* [maton github pr ready](./maton_github_pr_ready)
* [maton github pr reopen](./maton_github_pr_reopen)
* [maton github pr review](./maton_github_pr_review)
* [maton github pr search](./maton_github_pr_search)
* [maton github pr status](./maton_github_pr_status)
* [maton github pr update-branch](./maton_github_pr_update-branch)
* [maton github pr view](./maton_github_pr_view)


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
$ maton github pr view 123 --repo maton-ai/cli
$ maton github pr create --repo maton-ai/cli --base main --head feature --title "New thing"
$ maton github pr merge 123 --repo maton-ai/cli --squash
{% endraw %}{% endhighlight %}

### See also

* [maton github](./maton_github)
