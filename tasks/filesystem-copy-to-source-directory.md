---
title: "FileSystem.CopyToSourceDirectory"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes files and folders and copies them to the directory where dragged files originate.

**FileSystem.CopyToSourceDirectory** also passes its input to its output directory as it is, so you can put another *Task* behind it.

Note: If you drag & dropped files from **Finder** that are located in **different folders**, say `~/Downloads/some-song.mp3` and `~/Documents/notes.txt` there is no common source directory there the output could be copied to. If you also didn't specify a `fallback_path` the *Task* will throw an error and fail in these cases.

## Arguments

- **overwrite_existing** (optional) is a *boolean* that determines what should happen if a file or folder of the same name already exists at the target location: If set to *False* the *Task* throws an error and exits. If set to *True* it overwrites the file/folder and continues.

```python
# overwrite_existing = False  # default
overwrite_existing = True
```

- **fallback_path** is a *string* of the full path that should be used if the files have no common parent folder.

```python
# fallback_path = ''  # default
fallback_path = '/my/target/directory'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/FileSystem.CopyToSourceDirectory/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
