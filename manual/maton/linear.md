---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear

Manage issues, projects, and teams in Linear.

### Resource commands

* [maton linear comment](/manual/maton/linear/comment)
* [maton linear cycle](/manual/maton/linear/cycle)
* [maton linear issue](/manual/maton/linear/issue)
* [maton linear label](/manual/maton/linear/label)
* [maton linear org](/manual/maton/linear/org)
* [maton linear project](/manual/maton/linear/project)
* [maton linear state](/manual/maton/linear/state)
* [maton linear team](/manual/maton/linear/team)
* [maton linear user](/manual/maton/linear/user)


### Auth commands

* [maton linear whoami](/manual/maton/linear/whoami)


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
$ maton linear issue get MTN-527
$ maton linear issue create --team-id <uuid> -t 'Fix login'
$ maton linear comment create --issue MTN-527 -b 'Looking into this'
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
