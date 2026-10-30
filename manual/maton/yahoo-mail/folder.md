---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton yahoo-mail folder

IMAP mailboxes organise mail in folders rather than labels.

### Available commands

* [maton yahoo-mail folder create](/manual/maton/yahoo-mail/folder/create)
* [maton yahoo-mail folder delete](/manual/maton/yahoo-mail/folder/delete)
* [maton yahoo-mail folder list](/manual/maton/yahoo-mail/folder/list)
* [maton yahoo-mail folder rename](/manual/maton/yahoo-mail/folder/rename)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton yahoo-mail folders

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton yahoo-mail folder list
$ maton yahoo-mail folder create Receipts
$ maton yahoo-mail folder rename Receipts "Receipts 2026"
{% endraw %}{% endhighlight %}

### See also

* [maton yahoo-mail](/manual/maton/yahoo-mail)
