---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton icloud-mail folder

IMAP mailboxes organise mail in folders rather than labels.

### Available commands

* [maton icloud-mail folder create](/manual/maton/icloud-mail/folder/create)
* [maton icloud-mail folder delete](/manual/maton/icloud-mail/folder/delete)
* [maton icloud-mail folder list](/manual/maton/icloud-mail/folder/list)
* [maton icloud-mail folder rename](/manual/maton/icloud-mail/folder/rename)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton icloud-mail folders

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton icloud-mail folder list
$ maton icloud-mail folder create Receipts
$ maton icloud-mail folder rename Receipts "Receipts 2026"
{% endraw %}{% endhighlight %}

### See also

* [maton icloud-mail](/manual/maton/icloud-mail)
