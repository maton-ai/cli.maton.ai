---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive comment

Manage comments on a file (list, view, create, update, delete)

### Available commands

* [maton google-drive comment create](./maton_google-drive_comment_create)
* [maton google-drive comment delete](./maton_google-drive_comment_delete)
* [maton google-drive comment list](./maton_google-drive_comment_list)
* [maton google-drive comment update](./maton_google-drive_comment_update)
* [maton google-drive comment view](./maton_google-drive_comment_view)


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

* [maton google-drive](./maton_google-drive)
