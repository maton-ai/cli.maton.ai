---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube comment

List comment threads on videos

### Available commands

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
$ maton youtube comment list --video dQw4w9WgXcQ --order time
$ maton youtube comment list --video dQw4w9WgXcQ --limit 100
{% endraw %}{% endhighlight %}

### See also

* [maton youtube](/manual/maton/youtube)
