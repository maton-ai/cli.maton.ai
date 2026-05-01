---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linkedin

Manage posts, organizations, and ad campaigns in LinkedIn.

### Available commands

* [maton linkedin ad-account](/manual/maton/linkedin/ad-account)
* [maton linkedin campaign](/manual/maton/linkedin/campaign)
* [maton linkedin image](/manual/maton/linkedin/image)
* [maton linkedin organization](/manual/maton/linkedin/organization)
* [maton linkedin post](/manual/maton/linkedin/post)
* [maton linkedin whoami](/manual/maton/linkedin/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton linkedin whoami
$ maton linkedin post list --author urn:li:person:abc123
$ maton linkedin post create --author urn:li:person:abc123 --text 'Hello world'
$ maton linkedin organization list
$ maton linkedin ad-account list
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
