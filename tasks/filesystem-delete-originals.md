---
title: "FileSystem.DeleteOriginals"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* deletes the dropped files and folders at their original location.

**FileSystem.DeleteOriginals** also passes its input to its output directory as it is, so you can put another *Task* behind it.

Note: The **re-drop** functionality of *DropPy's* [Development Mode]({{< ref "general.md" >}}) usually fails for *Workflows* that use this *Task* because the files are not available any more (unless you manually restore them or write files with the same name to that location).

## Arguments

- **delete_to_trash** (optional) is a *boolean* that determines how to delete the files and folders. Set to *True* it uses *AppleScript* internally to delete them to macOS Trash (default). If you override this behavior by setting it to *False* the *Task* uses Python's `os.remove` function.

```python
# delete_to_trash = True  # default
delete_to_trash = False
```

{{% alert theme="warning" %}}**Danger zone**. Please be aware of what you're doing here. I don't want you to suffer data loss.{{% /alert %}}

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/FileSystem.DeleteOriginals/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://www.anthonysmith.me.uk/2008/01/08/moving-files-to-trash-from-the-mac-command-line/" target="_blank">Moving files to trash from Mac command line {{%icon fa-external-link-square%}}</a>
