---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton jira comment

List and add comments on issues

### Available commands

* [maton jira comment add](/manual/maton/jira/comment/add)
* [maton jira comment list](/manual/maton/jira/comment/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton jira comments

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton jira cloud list
$ maton jira comment list PROJ-123 --cloud-id <id>
$ maton jira comment add PROJ-123 --cloud-id <id> --body 'Looking into this'
$ cat note.md | maton jira comment add PROJ-123 --cloud-id <id> -F -
{% endraw %}{% endhighlight %}

### See also

* [maton jira](/manual/maton/jira)
