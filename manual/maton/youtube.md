---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube

Manage videos, playlists, and channels in YouTube.

### Available commands

* [maton youtube channel](/manual/maton/youtube/channel)
* [maton youtube comment](/manual/maton/youtube/comment)
* [maton youtube playlist](/manual/maton/youtube/playlist)
* [maton youtube search](/manual/maton/youtube/search)
* [maton youtube subscription](/manual/maton/youtube/subscription)
* [maton youtube video](/manual/maton/youtube/video)
* [maton youtube video-category](/manual/maton/youtube/video-category)
* [maton youtube whoami](/manual/maton/youtube/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton youtube whoami
$ maton youtube search videos 'go programming'
$ maton youtube video list --region US
$ maton youtube video view dQw4w9WgXcQ
$ maton youtube comment list --video dQw4w9WgXcQ
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
