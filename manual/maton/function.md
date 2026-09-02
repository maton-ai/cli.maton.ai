---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton function

Work with Maton functions: sandboxed HTTP handlers you deploy from a local
directory and invoke over a URL.

`deploy` is the command to reach for. It creates the function on its first
run and publishes a new version on every run after that, remembering which
function belongs to the directory so no ID has to be typed:

    $ cd my-fn && maton function deploy

`create` and `update` sit underneath it and map one-to-one onto POST and
PATCH. Prefer them in scripts, where an explicit ID and a single HTTP verb are
the point, and for the things deploy deliberately will not do — renaming a
function, or rolling back to an existing version.

A deployed function is an ordinary HTTP request handler, so any HTTP client
invokes it given the URL and a bearer token; `maton api` is a
convenience that takes the absolute URL and injects the credentials the
active profile already holds:

    $ maton api https://my-fn-3k9xq2v.maton.app -f name=ada

The response carries the run's ID in `X-Function-Run-Id`, so `-i` names the
exact run for `function run get` and `function run log list --run`.

# The handler contract

Every version records a handler, written `<module>.<symbol>`.
`main.handler` is `handler` in `main.py`, and `lib/util.handler`
is `handler` in `lib/util.py`. The module carries no extension; the
runtime supplies it.

It is called as `handler(event, context)`. Arguments are not bound by name
from the request: the whole request arrives as `event`, a Maton event
(version 1) carrying `rawPath`, `rawQueryString`, `cookies`, `headers`,
`queryStringParameters`, `requestContext`, `body`, and
`isBase64Encoded`. `requestContext.runId` names the run, and
`requestContext.http` carries the method, path, protocol, source IP, and
user agent. `body` is absent from a request that carries none and a
string whenever it is present, so it has to be read defensively and parsed:

    import json

    def handler(event, context):
        payload = json.loads(event.get("body") or "{}")
        return {"greeting": f"hi {payload.get('name')}"}

`context` carries `run_id`, `function_name`, `function_version`,
`function_id`, `account_id`, and `memory_limit_in_mb` (camelCase on
Node). A Python handler declaring one positional parameter is called with the
event alone.

The sandbox's environment is the variables from `function env` plus
`MATON_API_KEY`, which is runtime-provided.

# The response

Whatever the handler returns is JSON-encoded and sent as the body with a
`200`, so `return "hello"` answers with `"hello"` — quotes included.
The one exception is a dict carrying `statusCode`, which is read as an
envelope instead:

    def handler(event, context):
        return {
            "statusCode": 201,
            "headers": {"content-type": "text/plain"},
            "body": "created",
        }

A handler that raises answers `500` with the body `Internal Server Error`;
one that runs past the execution limit answers `504` with the same body.
Neither says why, so the run's logs are the diagnosis. A handler that cannot be
resolved at all never gets that far: it is a `400` from `create`,
`update`, or `deploy`, before anything is published.


### Available commands

* [maton function create](/manual/maton/function/create)
* [maton function delete](/manual/maton/function/delete)
* [maton function deploy](/manual/maton/function/deploy)
* [maton function get](/manual/maton/function/get)
* [maton function list](/manual/maton/function/list)
* [maton function search](/manual/maton/function/search)
* [maton function update](/manual/maton/function/update)


### Resource commands

* [maton function code](/manual/maton/function/code)
* [maton function env](/manual/maton/function/env)
* [maton function run](/manual/maton/function/run)
* [maton function version](/manual/maton/function/version)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


### ALIASES

maton functions

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ cd my-fn && maton function deploy
$ maton function list
$ maton function get 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function run log list --function 9f3c1e2a-0b7d-4c11-9d2e-5f6a7b8c9d01
$ maton function search '"def handler("'
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
