---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive reply

Manage replies to comments (list, view, create, update, delete)

### Available commands

* [maton google-drive reply create](./maton_google-drive_reply_create)
* [maton google-drive reply delete](./maton_google-drive_reply_delete)
* [maton google-drive reply list](./maton_google-drive_reply_list)
* [maton google-drive reply update](./maton_google-drive_reply_update)
* [maton google-drive reply view](./maton_google-drive_reply_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-drive replies

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-drive file list
$ maton google-drive comment list -f 1aBcD...
$ maton google-drive reply list -f 1aBcD... --comment cmt_xyz
$ maton google-drive reply create -f 1aBcD... --comment cmt_xyz --content 'Thanks'
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive](./maton_google-drive)
