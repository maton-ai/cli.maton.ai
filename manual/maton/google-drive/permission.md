---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-drive permission

Manage file/folder permissions (list, get, create, update, delete)

### Available commands

* [maton google-drive permission create](/manual/maton/google-drive/permission/create)
* [maton google-drive permission delete](/manual/maton/google-drive/permission/delete)
* [maton google-drive permission get](/manual/maton/google-drive/permission/get)
* [maton google-drive permission list](/manual/maton/google-drive/permission/list)
* [maton google-drive permission update](/manual/maton/google-drive/permission/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-drive permissions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-drive file list
$ maton google-drive permission list -f 1aBcD...
$ maton google-drive permission create -f 1aBcD... --type user --role writer --email-address alice@acme.com
$ maton google-drive permission delete <permission-id> -f 1aBcD...
{% endraw %}{% endhighlight %}

### See also

* [maton google-drive](/manual/maton/google-drive)
