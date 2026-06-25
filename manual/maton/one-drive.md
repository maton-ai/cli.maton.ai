---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton one-drive

Manage files and folders in OneDrive.

### Resource commands

* [maton one-drive drive](/manual/maton/one-drive/drive)
* [maton one-drive item](/manual/maton/one-drive/item)


### Auth commands

* [maton one-drive whoami](/manual/maton/one-drive/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton one-drive whoami
$ maton one-drive drive list
$ maton one-drive item list
$ maton one-drive item upload ./report.pdf --path Documents/report.pdf
$ maton one-drive drive search 'budget'
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
