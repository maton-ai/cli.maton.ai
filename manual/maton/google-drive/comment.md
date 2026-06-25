---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive comment

Manage comments on a file (list, get, create, update, delete)

### Available commands

* [maton google-drive comment create](/manual/maton/google-drive/comment/create)
* [maton google-drive comment delete](/manual/maton/google-drive/comment/delete)
* [maton google-drive comment get](/manual/maton/google-drive/comment/get)
* [maton google-drive comment list](/manual/maton/google-drive/comment/list)
* [maton google-drive comment update](/manual/maton/google-drive/comment/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-drive comments

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-drive file list
$ maton google-drive comment list -f 1aBcD...
$ maton google-drive comment create -f 1aBcD... --content 'Looks good'
$ maton google-drive comment delete <comment-id> -f 1aBcD...
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive](/manual/maton/google-drive)
