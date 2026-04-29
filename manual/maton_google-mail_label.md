---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail label

List, create, update, and delete labels

### Available commands

* [maton google-mail label create](./maton_google-mail_label_create)
* [maton google-mail label delete](./maton_google-mail_label_delete)
* [maton google-mail label list](./maton_google-mail_label_list)
* [maton google-mail label update](./maton_google-mail_label_update)
* [maton google-mail label view](./maton_google-mail_label_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton google-mail labels

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-mail label list
$ maton google-mail label view Label_123
$ maton google-mail label create --name 'Followup'
$ maton google-mail label update Label_123 --name 'Renamed'
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail](./maton_google-mail)
