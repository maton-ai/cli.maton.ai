---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack file

Manage files (upload, list, view, delete)

### Available commands

* [maton slack file delete](./maton_slack_file_delete)
* [maton slack file list](./maton_slack_file_list)
* [maton slack file upload](./maton_slack_file_upload)
* [maton slack file view](./maton_slack_file_view)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack file list
$ maton slack file upload --file ./report.pdf --channel C012
$ maton slack file view F0123456789
$ maton slack file delete F0123456789
{% endraw %}{% endhighlight %}

### See also

* [maton slack](./maton_slack)
