---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linkedin

Manage posts, organizations, and ad campaigns in LinkedIn.

### Available commands

* [maton linkedin ad-account](./maton_linkedin_ad-account)
* [maton linkedin campaign](./maton_linkedin_campaign)
* [maton linkedin image](./maton_linkedin_image)
* [maton linkedin organization](./maton_linkedin_organization)
* [maton linkedin post](./maton_linkedin_post)
* [maton linkedin whoami](./maton_linkedin_whoami)


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

* [maton](./maton)
