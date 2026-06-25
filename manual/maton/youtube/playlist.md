---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube playlist

List, get, create, update, delete, and manage playlist videos

### Available commands

* [maton youtube playlist add-video](/manual/maton/youtube/playlist/add-video)
* [maton youtube playlist create](/manual/maton/youtube/playlist/create)
* [maton youtube playlist delete](/manual/maton/youtube/playlist/delete)
* [maton youtube playlist get](/manual/maton/youtube/playlist/get)
* [maton youtube playlist items](/manual/maton/youtube/playlist/items)
* [maton youtube playlist list](/manual/maton/youtube/playlist/list)
* [maton youtube playlist remove-video](/manual/maton/youtube/playlist/remove-video)
* [maton youtube playlist update](/manual/maton/youtube/playlist/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton youtube playlists

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton youtube playlist list
$ maton youtube playlist items PLrAXtmRdnEQy6nuLMfO6JzeRBGroTkzmA
$ maton youtube playlist create --title "Study music"
$ maton youtube playlist update PL123 --title "Renamed"
$ maton youtube playlist delete PL123
$ maton youtube playlist add-video --playlist PL123 --video dQw4w9WgXcQ
$ maton youtube playlist remove-video PLI1
{% endraw %}{% endhighlight %}

### See also

* [maton youtube](/manual/maton/youtube)
