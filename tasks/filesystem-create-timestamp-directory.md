---
title: "FileSystem.CreateTimestampDirectory"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes files and folders and puts them in a timestamp sub-directory in its its output folder.

**FileSystem.CreateTimestampDirectory** uses the `datetime` module from Python's standard library internally.

## Arguments

- **name_pattern** (optional) is a *string* specifying how the date and time should be formatted in the directory that will be created. For a nice list of available directives see <a href="http://strftime.org" target="_blank">strftime.org {{%icon fa-external-link-square%}}</a>.

```python
# name_pattern = '%Y-%m-%d_%H%M%S'  # default
name_pattern = 'logfiles %d.%m.%Y'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/FileSystem.CreateTimestampDirectory/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://strftime.org" target="_blank">Python datetime cheat-sheet on strftime.org {{%icon fa-external-link-square%}}</a>
- <a href="https://docs.python.org/2/library/datetime.html" target="_blank">Official Python datetime documentation {{%icon fa-external-link-square%}}</a>
