---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive

Manage files, folders, and permissions in Google Drive.

### Available commands

* [maton google-drive about](./maton_google-drive_about)
* [maton google-drive comment](./maton_google-drive_comment)
* [maton google-drive drive](./maton_google-drive_drive)
* [maton google-drive file](./maton_google-drive_file)
* [maton google-drive permission](./maton_google-drive_permission)
* [maton google-drive reply](./maton_google-drive_reply)
* [maton google-drive revision](./maton_google-drive_revision)


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

* [maton](./maton)
