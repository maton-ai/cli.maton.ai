---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive drive

Manage shared drives (list, view, create, update, delete, hide, unhide)

### Available commands

* [maton google-drive drive create](./maton_google-drive_drive_create)
* [maton google-drive drive delete](./maton_google-drive_drive_delete)
* [maton google-drive drive hide](./maton_google-drive_drive_hide)
* [maton google-drive drive list](./maton_google-drive_drive_list)
* [maton google-drive drive unhide](./maton_google-drive_drive_unhide)
* [maton google-drive drive update](./maton_google-drive_drive_update)
* [maton google-drive drive view](./maton_google-drive_drive_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-drive drives

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-drive drive list
$ maton google-drive drive view 0AB...
$ maton google-drive drive create --name 'Team Drive'
$ maton google-drive drive update 0AB... --name 'Renamed Drive'
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive](./maton_google-drive)
