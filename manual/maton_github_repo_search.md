---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github repo search

```
maton github repo search [<query>...] [flags]
```

Searches /search/repositories. Positional args become free-text keywords;
flags are translated into qualifier syntax (language:go, topic:cli, etc.)
and joined into the q= parameter. At least one keyword or qualifier flag
must be set.

GitHub's search API caps results at 1000 across all pages and at 100 per
page, so --limit accepts 1-100. For the full qualifier vocabulary, build
the q string yourself in the positional args (e.g. 'maton github repo
search foo "size:<5000"').

### Options


<dl class="flags">
	<dt>
		<code>--archived &lt;string&gt;</code></dt>
	<dd>Filter by archived state: true or false</dd>

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
		<code>--language &lt;string&gt;</code></dt>
	<dd>Filter on coding language</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 30)</code></dt>
	<dd>Maximum results per page (1-100)</dd>

	<dt>
		<code>--order &lt;string&gt;</code></dt>
	<dd>Sort direction: asc or desc (only with --sort)</dd>

	<dt>
		<code>--owner &lt;string&gt;</code></dt>
	<dd>Filter on owner (user or org)</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt>
		<code>--sort &lt;string&gt;</code></dt>
	<dd>Sort by: stars, forks, help-wanted-issues, updated</dd>

	<dt>
		<code>--stars &lt;string&gt;</code></dt>
	<dd>Filter on number of stars (e.g. &#34;&gt;100&#34;, &#34;50..100&#34;)</dd>

	<dt>
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--topic &lt;string&gt;</code></dt>
	<dd>Comma-separated topics to match</dd>
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
$ maton github repo search cli shell
$ maton github repo search "vim plugin"
$ maton github repo search --owner microsoft --language go
$ maton github repo search --topic cli,terminal --stars ">100"
$ maton github repo search --owner github --archived false --sort stars
{% endraw %}{% endhighlight %}

### See also

* [maton github repo](./maton_github_repo)
