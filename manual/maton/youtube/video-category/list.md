---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton youtube video-category list

List video categories available in a region

```
maton youtube video-category list [flags]
```

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--language &lt;string&gt;</code></dt>
	<dd>BCP-47 language tag for localized titles (e.g. en, ko)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--region &lt;string&gt; (default &#34;US&#34;)</code></dt>
	<dd>Region code (e.g. US, KR, JP)</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton youtube video-category list
$ maton youtube video-category list --region KR
$ maton youtube video-category list --region US --language ko
{% endraw %}{% endhighlight %}

### See also

* [maton youtube video-category](/manual/maton/youtube/video-category)
