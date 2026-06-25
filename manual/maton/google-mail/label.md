---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton google-mail label

List, create, update, and delete labels

### Available commands

* [maton google-mail label create](/manual/maton/google-mail/label/create)
* [maton google-mail label delete](/manual/maton/google-mail/label/delete)
* [maton google-mail label get](/manual/maton/google-mail/label/get)
* [maton google-mail label list](/manual/maton/google-mail/label/list)
* [maton google-mail label update](/manual/maton/google-mail/label/update)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

 maton google-mail labels, maton gmail labels

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton google-mail label list
$ maton google-mail label get Label_123
$ maton google-mail label create --name 'Followup'
$ maton google-mail label update Label_123 --name 'Renamed'
{% endraw %}{% endhighlight %}

### See also

* [maton google-mail](/manual/maton/google-mail)
