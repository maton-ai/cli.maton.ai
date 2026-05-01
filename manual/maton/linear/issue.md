---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linear issue

Manage issues (list, view, search, create, update, delete)

### Available commands

* [maton linear issue create](/manual/maton/linear/issue/create)
* [maton linear issue delete](/manual/maton/linear/issue/delete)
* [maton linear issue list](/manual/maton/linear/issue/list)
* [maton linear issue search](/manual/maton/linear/issue/search)
* [maton linear issue update](/manual/maton/linear/issue/update)
* [maton linear issue view](/manual/maton/linear/issue/view)


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

* [maton linear](/manual/maton/linear)
