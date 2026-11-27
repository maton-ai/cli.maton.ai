---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton context graphql

```
maton context graphql [<graphql>] [flags]
```

Run one GraphQL query or mutation against your account's context and
print the response's data as JSON.

Pass the GraphQL as an argument, or read it with `--file`. To keep values
out of the GraphQL text, declare a variable such as `$first: Int` and
supply it with `--variable first=5`. A variable declared as `String` or
`ID` takes the value as is, so `--variable text=123` sends the string
"123" and `--variable text=null` sends the string "null"; to send null,
use `--variables '{"text": null}'`. Any other value that is valid JSON is
sent as that JSON, so numbers, booleans, null, lists, and objects work;
anything else is sent as a string. A number or boolean for a variable
declared as another scalar, such as `DateTime`, or as an enum or input
object, is sent as a string. `--variables` takes all variables at once as
a JSON object, or `@file` to read them from a file.

With `--paginate`, the query is repeated until there are no more pages,
and each page is printed as its own JSON document. The query must
accept an `$endCursor: String` variable, pass it as `after`, and select
`pageInfo { hasNextPage endCursor }` on that same field. Select those
three names without aliases. Only one field can take `$endCursor`,
so paginate one collection per query. Mutations cannot be paginated.

If the response has GraphQL errors, any partial data is still printed,
the errors go to standard error, and the exit status is non-zero.


### Options


<dl class="flags">
	<dt><code>-f</code>, 
		<code>--file &lt;file&gt;</code></dt>
	<dd>Read the GraphQL from file (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json</code></dt>
	<dd>Output raw JSON</dd>

	<dt>
		<code>--operation-name &lt;string&gt;</code></dt>
	<dd>Operation to run when the GraphQL defines several</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Make additional requests to fetch all pages of results</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--variable &lt;name=value&gt;</code></dt>
	<dd>Set a GraphQL variable in name=value format</dd>

	<dt>
		<code>--variables &lt;json&gt;</code></dt>
	<dd>Set all GraphQL variables from a json object (use &#34;@&lt;path&gt;&#34; to read it from a file)</dd>
</dl>


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton context gql

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
# Search nodes of any type
$ maton context graphql '{ search(query: "acme.com", first: 5) { nodes { __typename id } } }'

# With variables, printing only the IDs
$ maton context graphql 'query($text: String, $first: Int) { search(query: $text, first: $first) { nodes { id } } }' --variable text=acme.com --variable first=5 --json --jq '.search.nodes[].id'

# A query kept in a file
$ maton context graphql --file search.graphql --variables @variables.json

# Every page of a collection
$ maton context graphql --paginate --json --jq '.search.nodes[].id' '
  query($endCursor: String) {
    search(first: 100, after: $endCursor) {
      nodes { id }
      pageInfo { hasNextPage endCursor }
    }
  }
'

# Inspect the schema: list types, or the fields of one type
$ maton context graphql '{ __schema { types { name kind } } }'
$ maton context graphql '{ __type(name: "Query") { fields { name description } } }'

# Tag a node
$ maton context graphql 'mutation($ids: [ID!]!) { tag(ids: $ids, tags: ["follow-up"]) { id } }' --variable ids='["<node-id>"]'
{% endraw %}{% endhighlight %}

### See also

* [maton context](/manual/maton/context)
