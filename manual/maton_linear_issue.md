---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear issue

Manage issues (list, view, search, create, update, delete)

### Available commands

* [maton linear issue create](./maton_linear_issue_create)
* [maton linear issue delete](./maton_linear_issue_delete)
* [maton linear issue list](./maton_linear_issue_list)
* [maton linear issue search](./maton_linear_issue_search)
* [maton linear issue update](./maton_linear_issue_update)
* [maton linear issue view](./maton_linear_issue_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton linear issues

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton linear team list
$ maton linear issue list -c MTN -L 10
$ maton linear issue view MTN-527
$ maton linear issue create --team-id <uuid> -t 'Fix login'
{% endraw %}{% endhighlight %}

### See also

* [maton linear](./maton_linear)
