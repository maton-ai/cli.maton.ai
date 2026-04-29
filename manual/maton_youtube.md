---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube

Manage videos, playlists, and channels in YouTube.

### Available commands

* [maton youtube channel](./maton_youtube_channel)
* [maton youtube comment](./maton_youtube_comment)
* [maton youtube playlist](./maton_youtube_playlist)
* [maton youtube search](./maton_youtube_search)
* [maton youtube subscription](./maton_youtube_subscription)
* [maton youtube video](./maton_youtube_video)
* [maton youtube whoami](./maton_youtube_whoami)


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
$ maton youtube channel mine
$ maton youtube playlist list
$ maton youtube comment list --video dQw4w9WgXcQ
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
