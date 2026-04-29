---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive file

Manage files and folders (list, view, create, update, delete, copy, upload, download, export)

### Available commands

* [maton google-drive file copy](./maton_google-drive_file_copy)
* [maton google-drive file create](./maton_google-drive_file_create)
* [maton google-drive file delete](./maton_google-drive_file_delete)
* [maton google-drive file download](./maton_google-drive_file_download)
* [maton google-drive file empty-trash](./maton_google-drive_file_empty-trash)
* [maton google-drive file export](./maton_google-drive_file_export)
* [maton google-drive file generate-ids](./maton_google-drive_file_generate-ids)
* [maton google-drive file list](./maton_google-drive_file_list)
* [maton google-drive file update](./maton_google-drive_file_update)
* [maton google-drive file upload](./maton_google-drive_file_upload)
* [maton google-drive file view](./maton_google-drive_file_view)


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

* [maton google-drive](./maton_google-drive)
