---
title: "FileSystem.PatternCopyToDirectory"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes files and folders and copies them to another directory anywhere on your system - depending on the **Regular Expression** they match.

**FileSystem.PatternCopyToDirectory** also passes its input to its output directory as it is, so you can put another *Task* behind it.

Note: The file or folder will only be copied on the first match. If it happens to match another pattern down the line it won't be copied a second time. If it doesn't match any pattern it won't be copied at all.

## Arguments

- **patterns** (required) is a *list* of *strings* containing the **Regular Expression** to identify if a file should be copied. If a file matches it will be copied. The n-th pattern here matches to the n-th directory below.

```python
patterns = ['^.+\\.(jpg|jpeg|gif|png|tiff|psd)',
            '^.+\\.(m4a|mp3|ogg|flac)']
```

- **directories** (required) is a *list* of *strings* of the full paths to the directories that should receive the file/folder. The n-th pattern above matches to the n-th directory here. You need to have write permissions at that location.

```python
directories = ['~/Pictures',
               '~/Music']
```

- **ignore_case** (optional) is a *boolean* that influences the behavior of your **Regular Expressions**. If set to *True* the patterns are **case-INsensitive**. If set to *False* they are **case-sensitive**.

```python
# ignore_case = True  # default
ignore_case = False
```

- **overwrite_existing** (optiona) is a *boolean* that determines what should happen if a file or folder of the same name already exists at the target location: If set to *False* the *Task* throws an error and exits. If set to *True* it overwrites the file/folder and continues.

```python
# overwrite_existing = False  # default
overwrite_existing = True
```

- **create_directory** (optional) is a *boolean* that determines what should happen if the directory does not exist yet: If set to *False* and the *Task* throws an error and exits. If set to *True* it creates the directory and continues.

```python
# create_directory = False  # default
create_directory = True
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/FileSystem.PatternCopyToDirectory/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://regexr.com" target="_blank">RegExr - Regular Expressions build/test web tool {{%icon fa-external-link-square%}}</a>
