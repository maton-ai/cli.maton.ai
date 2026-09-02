---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function search

```
maton function search <query> [flags]
```

Search functions. The query argument carries its own mode syntax, and the mode
decides what is searched:

    stripe refund      ranked    name, description, and search text by
                                 lexical relevance. Does not read code.
    "def handler("     literal   code, as a fixed string. Only \" and \\
                                 are unescaped inside the quotes.
    /def\s+handler/    regex     code, as a regular expression. A bad
                                 pattern comes back as a 400.

The delimiters are parsed by the server, so quote them for your shell rather
than stripping them.

`--case` and `--context` apply to the two code modes only; the ranked mode
ignores them. `--case yes` means case-sensitive and `--case no` means
case-insensitive; the default `auto` is smartcase, i.e. case-sensitive
exactly when the pattern contains an uppercase letter.

Results are not paginated. Raising `--limit` is the only way to see more,
and the server caps it at 100. A `truncated` result means more functions
matched than were returned; it does not report recall limits applied while
scanning, which are invisible to clients.


### Options


<dl class="flags">
	<dt>
		<code>--case &lt;string&gt;</code></dt>
	<dd>Case sensitivity for code searches: {auto|yes|no}</dd>

	<dt>
		<code>--context &lt;int&gt; (default 0)</code></dt>
	<dd>Lines of context around each code hit</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-L</code>, 
		<code>--limit &lt;int&gt; (default 0)</code></dt>
	<dd>Maximum results, 0 for the server default of 25 (the server caps this at 100)</dd>

	<dt>
		<code>--owner &lt;string&gt;</code></dt>
	<dd>Whose functions to search: {SELF|ALL}</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--visibility &lt;string&gt;</code></dt>
	<dd>Filter by visibility: {PRIVATE|PUBLIC|UNLISTED}</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### JSON Fields

`account_id`, `created_at`, `description`, `function_id`, `hit_count`, `hits`, `name`, `network_policy`, `runtime`, `star_count`, `updated_at`, `url`, `version`, `view_count`, `visibility`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# Ranked search over names and descriptions
$ maton function search 'stripe refund'

# Literal code search, with two lines of context
$ maton function search '"def handler("' --context 2

# Regex code search across the public corpus
$ maton function search '/def\s+handler/' --owner ALL
{% endraw %}{% endhighlight %}

### See also

* [maton function](/manual/maton/function)
