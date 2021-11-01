# Mercurial

Displays information about local mercurial repositories: branch, changed
files, and recent commits.

#### Branch

The name of the currently-active mercurial branch.

#### Changed Files

A list of all the files that have changed since the last
commit, and their status.

#### Recent Commits

A list of `n` recent commits, who committed it, and when.

## Configuration

```yaml
mercurial:
  commitCount: 5
  commitFormat: "[forestgreen]{rev}:{phase} [white]{desc|firstline|strip} [grey]{author|person} {date|age}[white]"
  enabled: true
  position:
    top: 0
    left: 3
    height: 2
    width: 2
  refreshInterval: 8s
  repositories:
  - "/Users/user/fakelib"
  - "/Users/user/fakeapp"
```

## Screenshots

<img class="screenshot" src="/assets/modules/mercurial.png" width="710" height="248" alt="mercurial screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="commitCount", desc="The number of past commits to display.", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="commitFormat", desc="<code>Optional</code> The string format for the commit message." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="repositories", desc="A list of Mercurial repositories to watch.", value="A list of zero or more local file paths pointing to valid mercurial repositories." %}
            {% include "attributes/custom.md" %}
        {% endwith %}
    </tbody>
</table>

## Keyboard

<table>
  {% include "keyboard/table_header.md" %}

  <tbody>
    {% include "keyboard/foreslash.md" %}

    {% include "keyboard/spacer.md" %}

    {% set h="Show the previous Mercurial repository" %}
    {% include "keyboard/h.md" %}

    {% set l="Show the next Mercurial repository" %}
    {% include "keyboard/l.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous Mercurial repository" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next Mercurial repository" %}
    {% include "keyboard/arrowFore.md" %}
  </tbody>
</table>

{% set src="mercurial" %}
{% include "src_path.md" %}