---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-calendar settings

Per-user Calendar settings

### Available commands

* [maton google-calendar settings list](./maton_google-calendar_settings_list)
* [maton google-calendar settings view](./maton_google-calendar_settings_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-calendar settings list
$ maton google-calendar settings view timezone
$ maton google-calendar settings view locale
{% endraw %}{% endhighlight %}

### See also

* [maton google-calendar](./maton_google-calendar)
