---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton

The official command-line tool to interact with Maton.

### App commands

* [maton asana](./maton_asana)
* [maton github](./maton_github)
* [maton google-ads](./maton_google-ads)
* [maton google-calendar](./maton_google-calendar)
* [maton google-docs](./maton_google-docs)
* [maton google-drive](./maton_google-drive)
* [maton google-mail](./maton_google-mail)
* [maton google-sheets](./maton_google-sheets)
* [maton google-tasks](./maton_google-tasks)
* [maton hubspot](./maton_hubspot)
* [maton jira](./maton_jira)
* [maton linear](./maton_linear)
* [maton linkedin](./maton_linkedin)
* [maton microsoft-teams](./maton_microsoft-teams)
* [maton notion](./maton_notion)
* [maton one-drive](./maton_one-drive)
* [maton outlook](./maton_outlook)
* [maton salesforce](./maton_salesforce)
* [maton slack](./maton_slack)
* [maton stripe](./maton_stripe)
* [maton trello](./maton_trello)
* [maton youtube](./maton_youtube)


### Resource commands

* [maton connection](./maton_connection)


### Additional commands

* [maton alias](./maton_alias)
* [maton api](./maton_api)
* [maton completion](./maton_completion)
* [maton config](./maton_config)
* [maton login](./maton_login)
* [maton logout](./maton_logout)
* [maton whoami](./maton_whoami)


### Options


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>

	<dt>
		<code>--version</code></dt>
	<dd>Show maton version</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton login
$ maton connection list
$ maton google-mail message list -L 5
$ maton slack message send --channel C0123456789 --text 'Hello team'
$ maton api /google-mail/gmail/v1/users/me/messages
{% endraw %}{% endhighlight %}

