---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton linkedin image upload-init

```
maton linkedin image upload-init [flags]
```

Step 1 of LinkedIn's two-step image upload. POSTs to
/rest/images?action=initializeUpload and returns an upload URL plus
the image URN. PUT your image bytes to the returned uploadUrl, then
reference the image URN in a post's content.media block.

--owner accepts a URN (urn:li:person:<id> or urn:li:organization:<id>).
When omitted, the authenticated user's person URN is fetched from
/me automatically.

### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (Maton-Connection header)</dd>

	<dt>
		<code>--dry-run</code></dt>
	<dd>Print the request that would be sent without executing it</dd>

	<dt>
		<code>--format &lt;string&gt;</code></dt>
	<dd>Output format: &#39;json&#39; (default) or &#39;text&#39; on supported commands</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--owner &lt;string&gt;</code></dt>
	<dd>Owner URN (defaults to urn:li:person:&lt;id&gt; from /me)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
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
$ maton linkedin image upload-init
$ maton linkedin images upload-init --owner urn:li:organization:12345
{% endraw %}{% endhighlight %}

### See also

* [maton linkedin image](./maton_linkedin_image)
