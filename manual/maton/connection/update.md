---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton connection update

```
maton connection update <id> [flags]
```

Replace the access policy of an app connection. It applies immediately to every call made
through the connection. Pass it as JSON with --access-policy, or from a file (or - for
stdin) with --access-policy-file. null removes every restriction.

A policy looks like {"allow": [{"method": "GET", "path": "gmail/v1/users/*/messages/**"}], "deny": []}:
a call must match an allow rule and no deny rule. method is an HTTP method or *; path is
relative to the app, where * or {name} matches one segment (in an allow rule, not one ending
in a :verb custom method such as files/abc:export), {id}:verb matches that custom method,
and a trailing ** matches the rest.

Use --yes to skip the confirmation prompt (required when running non-interactively).


### Options


<dl class="flags">
	<dt>
		<code>--access-policy &lt;string&gt;</code></dt>
	<dd>Access policy as JSON, or null for full access</dd>

	<dt><code>-F</code>, 
		<code>--access-policy-file &lt;file&gt;</code></dt>
	<dd>Read the access policy from a JSON file (use - for stdin)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--yes</code></dt>
	<dd>Skip confirmation prompt</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### JSON Fields

`access_policy`, `app`, `connection_id`, `creation_time`, `granted_scopes`, `last_updated_time`, `metadata`, `method`, `status`, `status_reason`, `url`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton connection update conn_abc123 --access-policy '{"allow": [{"method": "GET", "path": "**"}]}'
$ maton connection update conn_abc123 --access-policy-file policy.json
$ cat policy.json | maton connection update conn_abc123 --access-policy-file -
$ maton connection update conn_abc123 --access-policy null --yes
{% endraw %}{% endhighlight %}

### See also

* [maton connection](/manual/maton/connection)
