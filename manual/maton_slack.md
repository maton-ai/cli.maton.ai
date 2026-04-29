---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton slack

Manage messages, channels, and users in Slack.

### Available commands

* [maton slack bot](./maton_slack_bot)
* [maton slack channel](./maton_slack_channel)
* [maton slack conversation](./maton_slack_conversation)
* [maton slack file](./maton_slack_file)
* [maton slack message](./maton_slack_message)
* [maton slack pin](./maton_slack_pin)
* [maton slack reaction](./maton_slack_reaction)
* [maton slack schedule](./maton_slack_schedule)
* [maton slack search](./maton_slack_search)
* [maton slack star](./maton_slack_star)
* [maton slack user](./maton_slack_user)
* [maton slack whoami](./maton_slack_whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton slack message send --channel C0123456789 --text 'Hello team'
$ maton slack channel list --types public_channel,private_channel
$ maton slack user lookup --email alice@example.com
$ maton slack reaction add --channel C012 --ts 1700000000.000100 --emoji thumbsup
{% endraw %}{% endhighlight %}

### See also

* [maton](./maton)
