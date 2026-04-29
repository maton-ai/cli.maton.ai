---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack pin

List, add, and remove pinned messages

### Available commands

* [maton slack pin add](./maton_slack_pin_add)
* [maton slack pin list](./maton_slack_pin_list)
* [maton slack pin remove](./maton_slack_pin_remove)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton slack pins

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack pin list C0123456789
$ maton slack pin add --channel C012 --ts 1700000000.000100
$ maton slack pin remove --channel C012 --ts 1700000000.000100
{% endraw %}{% endhighlight %}

### See also

* [maton slack](./maton_slack)
