---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton icloud-mail

Read, send, and organise mail in iCloud Mail over IMAP and SMTP.

Message IDs are "<folder>/<uid>", e.g. INBOX/124. A message's ID changes when it
moves to another folder; commands that move a message print its new ID.

iCloud Mail needs the Maton bridge running on your computer: install it once with
"maton bridge install". Commands that need it say so when it isn't running. With
bridges on more than one computer, pick one with --bridge <bridge-id>.


### Resource commands

* [maton icloud-mail draft](/manual/maton/icloud-mail/draft)
* [maton icloud-mail folder](/manual/maton/icloud-mail/folder)
* [maton icloud-mail message](/manual/maton/icloud-mail/message)
* [maton icloud-mail thread](/manual/maton/icloud-mail/thread)


### Auth commands

* [maton icloud-mail whoami](/manual/maton/icloud-mail/whoami)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### Examples

{% highlight bash %}{% raw %}
$ maton icloud-mail whoami
$ maton icloud-mail message list -L 5
$ maton icloud-mail message get INBOX/124 --headers
$ maton icloud-mail message send --to a@b.com --subject Hi --body 'Hello!'
$ maton icloud-mail folder list
{% endraw %}{% endhighlight %}

### See also

* [maton](/manual/maton)
