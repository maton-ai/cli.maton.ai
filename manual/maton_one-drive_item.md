---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive item

Browse and manage drive items (files and folders)

### Available commands

* [maton one-drive item copy](./maton_one-drive_item_copy)
* [maton one-drive item create-folder](./maton_one-drive_item_create-folder)
* [maton one-drive item delete](./maton_one-drive_item_delete)
* [maton one-drive item list](./maton_one-drive_item_list)
* [maton one-drive item move](./maton_one-drive_item_move)
* [maton one-drive item share](./maton_one-drive_item_share)
* [maton one-drive item upload](./maton_one-drive_item_upload)
* [maton one-drive item view](./maton_one-drive_item_view)
* [maton one-drive item view-by-path](./maton_one-drive_item_view-by-path)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton one-drive items

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton one-drive item list
$ maton one-drive item view 01ABCDEF
$ maton one-drive item upload ./report.pdf --path Documents/report.pdf
$ maton one-drive item delete 01ABCDEF
{% endraw %}{% endhighlight %}

### See also

* [maton one-drive](./maton_one-drive)
