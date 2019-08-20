---
title: "FileSystem.Rename"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes files and folders and renames them.

**FileSystem.Rename** optionally uses the `datetime` module from Python's standard library to prefix a timestamp.

Note: If the name is already in use a counter will be appended.

## Arguments

- **name** (required) is a *string* specifying the new name (including extension) of the file or folder.

```python
name = '_logfiles'
```

- **timestamp_prefix** (optional) is a *boolean* that controls if the *name* should be prefixed with a timestamp.

```python
# timestamp_prefix = False  # default
timestamp_prefix = True
```

- **timestamp_pattern** (optional) is a *string* specifying how the date and time should be formatted if *timestamp_prefix* is set to *True*. For a nice list of available directives see <a href="http://strftime.org" target="_blank">strftime.org</a>.

```python
# timestamp_pattern = '%Y-%m-%d_%H%M%S'  # default
timestamp_pattern = '%Y-%m'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/FileSystem.Rename/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://strftime.org" target="_blank">Python datetime cheat-sheet on strftime.org {{%icon fa-external-link-square%}}</a>
- <a href="https://docs.python.org/2/library/datetime.html" target="_blank">Official Python datetime documentation {{%icon fa-external-link-square%}}</a>
