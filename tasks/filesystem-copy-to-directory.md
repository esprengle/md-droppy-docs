---
title: "FileSystem.CopyToDirectory"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes files and folders and copies them to another directory anywhere on your system.

**FileSystem.CopyToDirectory** also passes its input to its output directory as it is, so you can put another *Task* behind it.

## Arguments

- **directory** (required) is a *string* of the full path to the directory that should receive all the content. You need to have write permissions at that location.

```python
directory = '/my/target/directory'
```

- **create_directory** (optional) is a *boolean* that determines what should happen if the directory does not exist yet: If set to *False* and the *Task* throws an error and exits. If set to *True* it creates the directory and continues.

```python
# create_directory = False  # default
create_directory = True
```

- **overwrite_existing** (optiona) is a *boolean* that determines what should happen if a file or folder of the same name already exists at the target location: If set to *False* the *Task* throws an error and exits. If set to *True* it overwrites the file/folder and continues.

```python
# overwrite_existing = False  # default
overwrite_existing = True
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/FileSystem.CopyToDirectory/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
