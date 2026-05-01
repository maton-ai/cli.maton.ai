---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive

Manage files, folders, and permissions in Google Drive.

### Available commands

* [maton google-drive about](/manual/maton/google-drive/about)
* [maton google-drive comment](/manual/maton/google-drive/comment)
* [maton google-drive drive](/manual/maton/google-drive/drive)
* [maton google-drive file](/manual/maton/google-drive/file)
* [maton google-drive permission](/manual/maton/google-drive/permission)
* [maton google-drive reply](/manual/maton/google-drive/reply)
* [maton google-drive revision](/manual/maton/google-drive/revision)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-drive file list -Q "name contains 'budget'"
$ maton google-drive file upload ./report.pdf --parent FOLDER_ID
$ maton google-drive permission create -f FILE_ID --type user --role writer --email-address alice@acme.com
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
