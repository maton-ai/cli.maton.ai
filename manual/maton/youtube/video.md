---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube video

List, get, and rate videos

### Available commands

* [maton youtube video get](/manual/maton/youtube/video/get)
* [maton youtube video list](/manual/maton/youtube/video/list)
* [maton youtube video rate](/manual/maton/youtube/video/rate)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton youtube videos

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton youtube video list
$ maton youtube video get dQw4w9WgXcQ
$ maton youtube video rate dQw4w9WgXcQ --rating like
{% endraw %}{% endhighlight %}

### See also

* [maton youtube](/manual/maton/youtube)
