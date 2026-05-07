---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton alias import

```
maton alias import [<filename> | -] [flags]
```

Import aliases from the contents of a YAML file.

Aliases should be defined as a map in YAML, where the keys represent aliases and
the values represent the corresponding expansions. An example file should look like
the following:

    bugs: github issue list --label=bug
    igrep: '!maton github issue list --label="$1" | grep "$2"'
    features: |-
        github issue list
        --label=enhancement

Use `-` to read aliases (in YAML format) from standard input.

The output from `maton alias list` can be used to produce a YAML file
containing your aliases, which you can use to import them from one machine to
another. Run `maton help alias list` to learn more.


### Options


<dl class="flags">
	<dt>
		<code>--clobber</code></dt>
	<dd>Overwrite existing aliases of the same name</dd>
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
# Import aliases from a file
$ maton alias import aliases.yml

# Import aliases from standard input
$ maton alias import -
{% endraw %}{% endhighlight %}

### See also

* [maton alias](/manual/maton/alias)
