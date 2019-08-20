---
title: "Filter.ByExtensions"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

Your *Task* may for example only be able to work with JPG files but not TXT files. Put **Filter.ByExtensions** in front of it to make sure only the right files get through.

This **works across sub-directories**: Dropping a folder structure that contains JPG and TXT files in several levels will result in the same folder structure, but only with the JPG files.

Note: Filtering by file extension is not the same thing as filtering by extracted data type / UTI. Use the *Task* [Filter.ByUTIs]({{<ref "filter-by-utis.md">}}) for this.

## Arguments

- **extensions** (optional) is a *list* of *strings* that contain the extensions that should get passed on to this *Task*'s output directory. All other files will be not be available for the next *Task*.
    - Capitalisation does not matter.
    - Do not pass a preceding dot.

```python
# extensions = ['txt', 'json', 'xml']  # default
extensions = ['jpg']
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Filter.ByExtensions/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
