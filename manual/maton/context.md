---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton context

Query the state Maton has observed in your apps through
gateway: objects such as messages, threads, issues, and files,
the relations between them, and the tags and metadata you attached.

`graphql` runs a GraphQL query or mutation. The main entry points are:

  search    nodes of any type, by text, type, filter, or change time
  node      one node by ID; `nodes` takes several
  tags      the tag names in use

Mutations annotate nodes without touching your apps: tag, untag,
setTags, setMetadata, and unsetMetadata.

The schema supports introspection: query `__schema` or `__type` to list
types, fields, and arguments.

Collections are paged with `first` and `after`, 50 items by default and
at most 100. Requests are limited to 10 per second per account.


### Available commands

* [maton context graphql](/manual/maton/context/graphql)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton context graphql '{ search(query: "acme.com", first: 5) { nodes { __typename id } } }'
$ maton context graphql --file changed.graphql --variable since=2026-11-01
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
