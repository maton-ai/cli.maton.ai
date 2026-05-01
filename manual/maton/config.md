---
layout: manual
permalink: /:path/:basename
---

{% raw %}## maton config

Display or change configuration settings for maton.

Current respected settings:
- `editor`: the text editor program to use for authoring text
- `prompt`: toggle interactive prompting in the terminal `{enabled | disabled}` (default `enabled`)
- `prefer_editor_prompt`: toggle preference for editor-based interactive prompting in the terminal `{enabled | disabled}` (default `disabled`)
- `pager`: the terminal pager program to send standard output to
- `http_unix_socket`: the path to a Unix socket through which to make an HTTP connection
- `browser`: the web browser to use for opening URLs
- `color_labels`: whether to display labels using their RGB hex color codes in terminals that support truecolor `{enabled | disabled}` (default `disabled`)
- `accessible_colors`: whether customizable, 4-bit accessible colors should be used `{enabled | disabled}` (default `disabled`)
- `accessible_prompter`: whether an accessible prompter should be used `{enabled | disabled}` (default `disabled`)
- `spinner`: whether to use a animated spinner as a progress indicator `{enabled | disabled}` (default `enabled`)
- `telemetry`: whether telemetry is enabled, disabled, or logging `{enabled | disabled | log}` (default `enabled`)


### Available commands

* [maton config clear-cache](/manual/maton/config/clear-cache)
* [maton config get](/manual/maton/config/get)
* [maton config list](/manual/maton/config/list)
* [maton config set](/manual/maton/config/set)


### Options inherited from parent commands


<dl class="flags">
	<dt><code>-p</code>, 
		<code>--profile &lt;string&gt;</code></dt>
	<dd>Profile to use for this invocation (overrides the active profile; also reads MATON_PROFILE)</dd>
</dl>


{% endraw %}
### See also

* [maton](/manual/maton)
