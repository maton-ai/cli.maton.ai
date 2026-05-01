---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton api

```
maton api <endpoint> [flags]
```

Makes an authenticated HTTP request to the Maton API and prints the response.

The endpoint argument should be a path of a Maton API endpoint.

The default HTTP request method is `GET` normally and `POST` if any parameters
were added. Override the method with `--method`.

Pass one or more `-f/--raw-field` values in `key=value` format to add static string
parameters to the request payload. To add non-string values, see `-F/--field` below.
Note that adding request parameters will automatically switch the request method to
`POST`. To send the parameters as a `GET` query string instead, use `--method GET`.

The `-F/--field` flag has magic type conversion based on the format of the value:

- literal values `true`, `false`, `null`, and integer numbers get converted to
  appropriate JSON types;
- if the value starts with `@`, the rest of the value is interpreted as a
  filename to read the value from. Pass `-` to read from standard input.

To pass nested parameters in the request payload, use `key[subkey]=value` syntax when
declaring fields. To pass nested values as arrays, declare multiple fields with the
syntax `key[]=value1`, `key[]=value2`. To pass an empty array, use `key[]` without a
value.

To pass pre-constructed JSON or payloads in other formats, a request body may be read
from file specified by `--input`. Use `-` to read from standard input. When passing the
request body this way, any parameters specified via field flags are added to the query
string of the endpoint URL.

In `--paginate` mode, all pages of results will sequentially be requested until
there are no more pages of results. Each page is a separate JSON array or object.
Pass `--slurp` to wrap all pages of JSON arrays or objects into an outer JSON array.


### Options


<dl class="flags">
	<dt>
		<code>--connection &lt;string&gt;</code></dt>
	<dd>Connection ID to route through (sets Maton-Connection header)</dd>

	<dt><code>-F</code>, 
		<code>--field &lt;key=value&gt;</code></dt>
	<dd>Add a typed parameter in key=value format (use &#34;@&lt;path&gt;&#34; or &#34;@-&#34; to read value from file or stdin)</dd>

	<dt><code>-H</code>, 
		<code>--header &lt;key:value&gt;</code></dt>
	<dd>Add a HTTP request header in key:value format</dd>

	<dt>
		<code>--hostname &lt;string&gt;</code></dt>
	<dd>The Maton hostname for the request (default &#34;api.maton.ai&#34;)</dd>

	<dt><code>-i</code>, 
		<code>--include</code></dt>
	<dd>Include HTTP response status line and headers in the output</dd>

	<dt>
		<code>--input &lt;file&gt;</code></dt>
	<dd>The file to use as body for the HTTP request (use &#34;-&#34; to read from standard input)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;string&gt;</code></dt>
	<dd>Query to select values from the response using jq syntax</dd>

	<dt><code>-X</code>, 
		<code>--method &lt;string&gt; (default &#34;GET&#34;)</code></dt>
	<dd>The HTTP method for the request</dd>

	<dt>
		<code>--paginate</code></dt>
	<dd>Make additional HTTP requests to fetch all pages of results</dd>

	<dt><code>-f</code>, 
		<code>--raw-field &lt;key=value&gt;</code></dt>
	<dd>Add a string parameter in key=value format</dd>

	<dt>
		<code>--silent</code></dt>
	<dd>Do not print the response body</dd>

	<dt>
		<code>--slurp</code></dt>
	<dd>Use with &#34;--paginate&#34; to return an array of all pages of either JSON arrays or objects</dd>

	<dt><code>-t</code>, 
		<code>--template &lt;string&gt;</code></dt>
	<dd>Format JSON output using a Go template; see &#34;maton help formatting&#34;</dd>

	<dt>
		<code>--verbose</code></dt>
	<dd>Include full HTTP request and response in the output</dd>
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
# List your connections
$ maton api /connections

# Filter connections by app
$ maton api -X GET connections -f app=slack

# Use a JSON file as request body
$ maton api /connections --input file.json

# Set a custom HTTP header
$ maton api -H 'Accept: application/json' connections

# Print only specific fields from the response
$ maton api /connections --jq '.[].id'

# Use a template for the output
$ maton api /connections --template \
  '{{range .}}{{.id}} ({{.app | color "yellow"}}){{"\n"}}{{end}}'
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
