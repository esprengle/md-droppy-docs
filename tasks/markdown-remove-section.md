---
title: "Markdown.RemoveSection"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* parses a **Mardown file** and removes a section from its content.

**Markdown.RemoveSection** only uses **Regular Expressions** and therefore has no external dependencies.

Note: This *Task* can be used in combination with the *Task* [Markdown.AddToc]({{<ref "markdown-add-toc.md">}}) to rebuild a **Table of Contents** (by first removing it and then adding it again).

## Arguments

- **section_start_regex** (optional) is a *string* containing the **Regular Expression** to identify the line that constitutes the **start** of the section that should be removed.

```python
# section_start_regex = '^# TOC$'  # default
section_start_regex = '^# Content$'
```

- **section_end_regex** (optional) is a *string* containing the **Regular Expression** to identify the line that constitutes the **end** of the section that should be removed.

```python
# section_end_regex = '^---$'  # default
section_end_regex = '^$'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Markdown.RemoveSection/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://spec.commonmark.org/0.27/" target="_blank">Markdown spec {{%icon fa-external-link-square%}}</a>
- <a href="https://regexr.com" target="_blank">RegExr - Regular Expressions build/test web tool {{%icon fa-external-link-square%}}</a>
