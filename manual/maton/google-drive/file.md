---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive file

Manage files and folders (list, view, create, update, delete, copy, upload, download, export)

### Available commands

* [maton google-drive file copy](/manual/maton/google-drive/file/copy)
* [maton google-drive file create](/manual/maton/google-drive/file/create)
* [maton google-drive file delete](/manual/maton/google-drive/file/delete)
* [maton google-drive file download](/manual/maton/google-drive/file/download)
* [maton google-drive file empty-trash](/manual/maton/google-drive/file/empty-trash)
* [maton google-drive file export](/manual/maton/google-drive/file/export)
* [maton google-drive file generate-ids](/manual/maton/google-drive/file/generate-ids)
* [maton google-drive file list](/manual/maton/google-drive/file/list)
* [maton google-drive file update](/manual/maton/google-drive/file/update)
* [maton google-drive file upload](/manual/maton/google-drive/file/upload)
* [maton google-drive file view](/manual/maton/google-drive/file/view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-drive files

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-drive file list
$ maton google-drive file view 1aBcD...
$ maton google-drive file upload ./report.pdf
$ maton google-drive file download 1aBcD... --output ./report.pdf
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive](/manual/maton/google-drive)
