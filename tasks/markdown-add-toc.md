---
title: "Markdown.AddToc"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* parses a **Mardown file** and adds a hyperlinked **Table of Content** containing all levels of headlines to the beginning of the file.

**Markdown.AddToc** only uses **Regular Expressions** and therefore has no external dependencies.

The **Table of Contents** will be seperated from the rest of the content by also adding  `---`, a **horizonal rule**.

## Arguments

- **toc_header** (optional) is a *string* of the headline to use for the added *Table Of Contents*.

```python
# toc_header = '# Table of Contents'  # default
toc_header = '# Content'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Markdown.AddToc/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://spec.commonmark.org/0.27/" target="_blank">Markdown spec {{%icon fa-external-link-square%}}</a>
- <a href="https://regexr.com" target="_blank">RegExr - Regular Expressions build/test web tool {{%icon fa-external-link-square%}}</a>
