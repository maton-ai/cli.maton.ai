---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton github issue develop

```
maton github issue develop <number-or-url> [flags]
```

Create a linked branch for an issue, or list linked branches with --list. Without --base-branch the linked branch is created off the repo's default branch.

### Options


<dl class="flags">
	<dt>
		<code>--base-branch &lt;string&gt;</code></dt>
	<dd>Branch to base the new branch off</dd>

	<dt>
		<code>--base-repo &lt;string&gt;</code></dt>
	<dd>Repository to create the branch in (defaults to --repo)</dd>

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

	<dt><code>-l</code>, 
		<code>--list</code></dt>
	<dd>List linked branches instead of creating one</dd>

	<dt><code>-n</code>, 
		<code>--name &lt;string&gt;</code></dt>
	<dd>Branch name to create</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Follow next_cursor and concatenate all pages (list commands only)</dd>

	<dt><code>-R</code>, 
		<code>--repo &lt;owner/repo&gt;</code></dt>
	<dd>Target repository in owner/repo form (required)</dd>

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
$ maton github issue develop 123 --repo maton-ai/cli
$ maton github issue develop 123 --repo maton-ai/cli --name fix-login --base-branch main
$ maton github issue develop 123 --repo maton-ai/cli --list
{% endraw %}{% endhighlight %}

### See also

* [maton github issue](/manual/maton/github/issue)
