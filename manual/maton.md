---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton

The official command-line tool to interact with Maton.

### App commands

* [maton asana](/manual/maton/asana)
* [maton github](/manual/maton/github)
* [maton google-ads](/manual/maton/google-ads)
* [maton google-calendar](/manual/maton/google-calendar)
* [maton google-docs](/manual/maton/google-docs)
* [maton google-drive](/manual/maton/google-drive)
* [maton google-mail](/manual/maton/google-mail)
* [maton google-sheets](/manual/maton/google-sheets)
* [maton google-tasks](/manual/maton/google-tasks)
* [maton hubspot](/manual/maton/hubspot)
* [maton jira](/manual/maton/jira)
* [maton linear](/manual/maton/linear)
* [maton linkedin](/manual/maton/linkedin)
* [maton microsoft-teams](/manual/maton/microsoft-teams)
* [maton notion](/manual/maton/notion)
* [maton one-drive](/manual/maton/one-drive)
* [maton outlook](/manual/maton/outlook)
* [maton salesforce](/manual/maton/salesforce)
* [maton slack](/manual/maton/slack)
* [maton stripe](/manual/maton/stripe)
* [maton trello](/manual/maton/trello)
* [maton youtube](/manual/maton/youtube)


### Resource commands

* [maton connection](/manual/maton/connection)


### Auth commands

* [maton login](/manual/maton/login)
* [maton logout](/manual/maton/logout)
* [maton whoami](/manual/maton/whoami)


### Additional commands

* [maton alias](/manual/maton/alias)
* [maton api](/manual/maton/api)
* [maton completion](/manual/maton/completion)
* [maton config](/manual/maton/config)
* [maton upgrade](/manual/maton/upgrade)


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

