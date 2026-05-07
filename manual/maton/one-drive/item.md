---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive item

Browse and manage drive items (files and folders)

### Available commands

* [maton one-drive item copy](/manual/maton/one-drive/item/copy)
* [maton one-drive item create-folder](/manual/maton/one-drive/item/create-folder)
* [maton one-drive item delete](/manual/maton/one-drive/item/delete)
* [maton one-drive item invite](/manual/maton/one-drive/item/invite)
* [maton one-drive item list](/manual/maton/one-drive/item/list)
* [maton one-drive item move](/manual/maton/one-drive/item/move)
* [maton one-drive item share](/manual/maton/one-drive/item/share)
* [maton one-drive item update](/manual/maton/one-drive/item/update)
* [maton one-drive item upload](/manual/maton/one-drive/item/upload)
* [maton one-drive item view](/manual/maton/one-drive/item/view)
* [maton one-drive item view-by-path](/manual/maton/one-drive/item/view-by-path)


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

* [maton one-drive](/manual/maton/one-drive)
