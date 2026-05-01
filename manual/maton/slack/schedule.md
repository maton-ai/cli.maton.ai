---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack schedule

List, create, and delete scheduled messages

### Available commands

* [maton slack schedule create](/manual/maton/slack/schedule/create)
* [maton slack schedule delete](/manual/maton/slack/schedule/delete)
* [maton slack schedule list](/manual/maton/slack/schedule/list)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack schedule list
$ maton slack schedule create --channel C012 --text 'Standup in 5' --post-at 1734567890
$ maton slack schedule delete --channel C012 --id Q1234567890
{% endraw %}{% endhighlight %}

### See also

* [maton slack](/manual/maton/slack)
