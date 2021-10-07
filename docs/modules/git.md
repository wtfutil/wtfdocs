
![git](/assets/services/git.png){: align=left width=128 height=128}

# Git

Displays information about local git repositories: branch, changed
files, and recent commits.

#### Branch

The name of the currently-active git branch.

#### Changed Files

A list of all the files that have changed since the last
commit, and their status.

#### Recent Commits

A list of `n` recent commits, who committed it, and when.

## Configuration

```yaml
git:
  commitCount: 5
  commitFormat: "[forestgreen]%h [grey]%cd [white]%s [grey]%an[white]"
  dateFormat: "%H:%M %d %b %y"
  enabled: true
  position:
    top: 0
    left: 3
    height: 2
    width: 2
  refreshInterval: 8
  repositories:
  - "/Users/chris/go/src/github.com/wtfutil/wtf"
  - "/Users/user/fakeapp"
```

## Screenshots

<img class="screenshot" src="/assets/modules/git.png" width="720" height="292" alt="git screenshot" />

## Attributes

<table>
    {% include "attributes/table_header.md" %}

    <tbody>
        {% with name="branchInTitle", desc="<code>Optional</code> Whether to show branch name in title. <br />Default: <code>false</code>", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="commitCount", desc="", value="Any positive integer." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="commitFormat", desc="<code>Optional</code> The string format for the commit message." %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% include "attributes/dateFormat.md" %}

        {% with name="lastFolderTitle", desc="<code>Optional</code> Whether to show only last part of directory path instead of full path. <br />Default: <code>false</code>", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showFilesIfEmpty", desc="<code>Optional</code> Whether to show Changed Files section if no files have changed. <br />Default: <code>false</code>", value="<code>true</code>, <code>false</code>" %}
            {% include "attributes/custom.md" %}
        {% endwith %}

        {% with name="showModuleName", desc="<code>Optional</code> Whether to show 'Git - ' before information in title. <br />Default: <code>true</code>", value="<code>true</code>, <code>false</code>" %}
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

    {% set h="Show the previous git repository" %}
    {% include "keyboard/h.md" %}

    {% set l="Show the next git repository" %}
    {% include "keyboard/l.md" %}

    {% set p="Pull repo" %}
    {% include "keyboard/p.md" %}

    {% include "keyboard/r.md" %}

    {% include "keyboard/spacer.md" %}

    {% set arrowBack="Show the previous git repository" %}
    {% include "keyboard/arrowBack.md" %}

    {% set arrowFore="Show the next git repository" %}
    {% include "keyboard/arrowFore.md" %}
  </tbody>
</table>

{% set src="git" %}
{% include "src_path.md" %}