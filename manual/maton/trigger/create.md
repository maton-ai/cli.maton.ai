---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton trigger create

```
maton trigger create --source <source> --event-type <type> [flags]
```

Create a trigger that subscribes to a source's events of a given type. Attach destinations now with repeatable --destination flags, or later with `maton trigger destination create`. A trigger with no destination is pull-only: its events are stored and listable but not delivered.

Each source emits its own event types:
  time         schedule.elapsed
  google-mail  email.received
  slack        channel_message.received, direct_message.received, reaction.added
  notion       page.created, page.content_updated, comment.created
  stripe       charge.succeeded, invoice.paid, subscription.created, subscription.canceled, invoice.payment_failed
  hubspot      contact.created, contact.deleted, contact.updated, company.created, company.deleted, company.updated, deal.created, deal.deleted, deal.updated, deal.stage_changed, ticket.created, ticket.deleted, ticket.updated
  linear       issue.created, issue.status_changed, issue.opened
  calendly     invitee.created, invitee.canceled, invitee_no_show.created
  github       pull_request.opened, pull_request.merged, branch.pushed, release.published


### Options


<dl class="flags">
	<dt>
		<code>--connection-id &lt;string&gt;</code></dt>
	<dd>Connection ID used to subscribe</dd>

	<dt>
		<code>--description &lt;string&gt;</code></dt>
	<dd>Description</dd>

	<dt>
		<code>--destination &lt;stringArray&gt;</code></dt>
	<dd>Destination as a JSON object (repeatable)</dd>

	<dt>
		<code>--event-type &lt;string&gt;</code></dt>
	<dd>Event type to subscribe to (required)</dd>

	<dt><code>-q</code>, 
		<code>--jq &lt;expression&gt;</code></dt>
	<dd>Filter JSON output using a jq expression</dd>

	<dt>
		<code>--json &lt;fields&gt;</code></dt>
	<dd>Output JSON with the specified fields</dd>

	<dt>
		<code>--name &lt;string&gt;</code></dt>
	<dd>Human-readable name</dd>

	<dt>
		<code>--parameter &lt;stringArray&gt;</code></dt>
	<dd>Trigger parameter key=value pair (repeatable)</dd>

	<dt>
		<code>--source &lt;string&gt;</code></dt>
	<dd>Source app the trigger subscribes to (required). One of: time, google-mail, slack, notion, stripe, hubspot, linear, calendly, github</dd>

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


### JSON Fields

`connection_id`, `created_at`, `description`, `destinations`, `event_type`, `name`, `parameters`, `reason`, `source`, `status`, `trigger_id`, `updated_at`

{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton trigger create --source github --event-type pull_request.opened --connection-id conn_123
$ maton trigger create --source github --event-type pull_request.opened \
    --parameter repo=maton-ai/cli \
    --destination '{"url":"https://httpbin.org/post","method":"POST","name":"prod"}'
{% endraw %}{% endhighlight %}

### See also

* [maton trigger](/manual/maton/trigger)
