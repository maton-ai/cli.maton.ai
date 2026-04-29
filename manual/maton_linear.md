---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear

Manage issues, projects, and teams in Linear.

### Available commands

* [maton linear comment](./maton_linear_comment)
* [maton linear cycle](./maton_linear_cycle)
* [maton linear issue](./maton_linear_issue)
* [maton linear label](./maton_linear_label)
* [maton linear me](./maton_linear_me)
* [maton linear project](./maton_linear_project)
* [maton linear state](./maton_linear_state)
* [maton linear team](./maton_linear_team)
* [maton linear user](./maton_linear_user)
* [maton linear whoami](./maton_linear_whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton linear whoami
$ maton linear issue list -c MTN -L 10
$ maton linear issue view MTN-527
$ maton linear issue create --team-id <uuid> -t 'Fix login'
$ maton linear comment create --issue MTN-527 -b 'Looking into this'
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
