---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail thread

List, view, trash, and modify message threads

### Available commands

* [maton google-mail thread list](./maton_google-mail_thread_list)
* [maton google-mail thread modify](./maton_google-mail_thread_modify)
* [maton google-mail thread trash](./maton_google-mail_thread_trash)
* [maton google-mail thread untrash](./maton_google-mail_thread_untrash)
* [maton google-mail thread view](./maton_google-mail_thread_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-mail threads

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-mail thread list -L 10
$ maton google-mail thread view 18f1a2b3
$ maton google-mail thread trash 18f1a2b3
$ maton google-mail thread modify 18f1a2b3 --add-label STARRED
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail](./maton_google-mail)
