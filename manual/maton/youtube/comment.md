---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube comment

List, post, reply to, and delete comments

### Available commands

* [maton youtube comment create](/manual/maton/youtube/comment/create)
* [maton youtube comment delete](/manual/maton/youtube/comment/delete)
* [maton youtube comment list](/manual/maton/youtube/comment/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton youtube comments

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton youtube comment list --video dQw4w9WgXcQ
$ maton youtube comment create --video dQw4w9WgXcQ --text "Great video!"
$ maton youtube comment create --parent <commentId> --text "I agree"
$ maton youtube comment delete <commentId>
{% endraw %}{% endhighlight %}

### See also

* [maton youtube](/manual/maton/youtube)
