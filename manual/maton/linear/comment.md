---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear comment

Manage issue comments (list, create, update, delete)

### Available commands

* [maton linear comment create](/manual/maton/linear/comment/create)
* [maton linear comment delete](/manual/maton/linear/comment/delete)
* [maton linear comment list](/manual/maton/linear/comment/list)
* [maton linear comment update](/manual/maton/linear/comment/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton linear comments

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton linear comment list --issue MTN-527
$ maton linear comment create --issue MTN-527 -b 'Looking into this'
$ cat note.md | maton linear comment create --issue MTN-527 -F -
$ maton linear comment update <comment-uuid> -b 'Edited'
{% endraw %}{% endhighlight %}

### See also

* [maton linear](/manual/maton/linear)
