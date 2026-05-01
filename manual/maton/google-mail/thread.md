---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail thread

List, view, trash, and modify message threads

### Available commands

* [maton google-mail thread list](/manual/maton/google-mail/thread/list)
* [maton google-mail thread modify](/manual/maton/google-mail/thread/modify)
* [maton google-mail thread trash](/manual/maton/google-mail/thread/trash)
* [maton google-mail thread untrash](/manual/maton/google-mail/thread/untrash)
* [maton google-mail thread view](/manual/maton/google-mail/thread/view)


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

* [maton google-mail](/manual/maton/google-mail)
