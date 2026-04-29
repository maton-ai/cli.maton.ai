---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive revision

Manage file revisions (list, view, update, delete)

### Available commands

* [maton google-drive revision delete](./maton_google-drive_revision_delete)
* [maton google-drive revision list](./maton_google-drive_revision_list)
* [maton google-drive revision update](./maton_google-drive_revision_update)
* [maton google-drive revision view](./maton_google-drive_revision_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-drive revisions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-drive file list
$ maton google-drive revision list -f 1aBcD...
$ maton google-drive revision view <revision-id> -f 1aBcD...
$ maton google-drive revision update <revision-id> -f 1aBcD... --keep-forever true
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive](./maton_google-drive)
