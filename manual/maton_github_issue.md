---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue

Create, view, list, and edit issues

### Available commands

* [maton github issue close](./maton_github_issue_close)
* [maton github issue comment](./maton_github_issue_comment)
* [maton github issue create](./maton_github_issue_create)
* [maton github issue delete](./maton_github_issue_delete)
* [maton github issue develop](./maton_github_issue_develop)
* [maton github issue edit](./maton_github_issue_edit)
* [maton github issue list](./maton_github_issue_list)
* [maton github issue lock](./maton_github_issue_lock)
* [maton github issue pin](./maton_github_issue_pin)
* [maton github issue reopen](./maton_github_issue_reopen)
* [maton github issue search](./maton_github_issue_search)
* [maton github issue status](./maton_github_issue_status)
* [maton github issue transfer](./maton_github_issue_transfer)
* [maton github issue unlock](./maton_github_issue_unlock)
* [maton github issue unpin](./maton_github_issue_unpin)
* [maton github issue view](./maton_github_issue_view)


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
$ maton github issue view 123 --repo maton-ai/cli
$ maton github issue create --repo maton-ai/cli --title "Bug" --body "..."
$ maton github issue close 123 --repo maton-ai/cli
{% endraw %}{% endhighlight %}

### See also

* [maton github](./maton_github)
