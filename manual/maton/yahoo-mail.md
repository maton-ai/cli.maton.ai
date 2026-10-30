---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton yahoo-mail

Read, send, and organise mail in Yahoo Mail over IMAP and SMTP.

Message IDs are the server's EMAILIDs (RFC 8474), e.g. AASdfpO5xHnhSafuAprfE24JZdM.
They stay the same when a message moves. Commands look for the message in --folder
(INBOX unless the command says otherwise) and fail if it isn't there.


### Resource commands

* [maton yahoo-mail draft](/manual/maton/yahoo-mail/draft)
* [maton yahoo-mail folder](/manual/maton/yahoo-mail/folder)
* [maton yahoo-mail message](/manual/maton/yahoo-mail/message)
* [maton yahoo-mail thread](/manual/maton/yahoo-mail/thread)


### Auth commands

* [maton yahoo-mail whoami](/manual/maton/yahoo-mail/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton yahoo-mail whoami
$ maton yahoo-mail message list -L 5
$ maton yahoo-mail message get AASdfpO5xHnhSafuAprfE24JZdM --headers
$ maton yahoo-mail message send --to a@b.com --subject Hi --body 'Hello!'
$ maton yahoo-mail folder list
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
