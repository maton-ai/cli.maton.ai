---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack bookmark

List, add, edit, and remove channel bookmarks

### Available commands

* [maton slack bookmark add](/manual/maton/slack/bookmark/add)
* [maton slack bookmark edit](/manual/maton/slack/bookmark/edit)
* [maton slack bookmark list](/manual/maton/slack/bookmark/list)
* [maton slack bookmark remove](/manual/maton/slack/bookmark/remove)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton slack bookmarks

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack bookmark list --channel C0123456789
$ maton slack bookmark add --channel C012 --title Runbook --link https://example.com/runbook
$ maton slack bookmark edit --channel C012 --bookmark-id Bk0123 --title 'New title'
$ maton slack bookmark remove --channel C012 --bookmark-id Bk0123
{% endraw %}{% endhighlight %}

### See also

* [maton slack](/manual/maton/slack)
