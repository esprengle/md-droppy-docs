---
title: "Text.Append"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* iterates over the files and folders passed to its input and appends their text to a fixed target file.

**Text.Append** can be used with any kind of text file (markdown, csv, log).

## Arguments

- **target_file** (required) is a *string* of the full path to the file that should receive all the content. The file (and the parent folder strucutre) will be created if it doesn't exist. You need to have write permissions at that location.

```python
target_file = '/my/target/is/here.txt'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Text.Append/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
