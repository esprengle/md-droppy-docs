---
title: "MacOS.OpenFilesInApp"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes files and opens them in an application installed on your system.

Internally **MacOS.OpenFilesInApp** uses *AppleScript*:

```bash
/usr/bin/osascript -e "tell app \"Your App Name\" to open POSIX file \"/path/to/your/file\""
```

## Arguments

- **app_name** (required) is a *string* of the name of the app to open.

```python
app_name = 'Sublime Text'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/MacOS.OpenFilesInApp/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
