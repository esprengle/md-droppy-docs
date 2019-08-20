---
title: "Filter.OnlyFiles"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

*Tasks* may be written in a way to **only handle paths to files** like `/Users/your-user-name/Documents/note.txt`, but **not paths refering to directories** like `/Users/your-user-name/Downloads/`.

To ensure the *Task* afterwards only received paths to files put **Filter.OnlyFiles** before it. You then don't have to check each path inside your *Task* to make sure it refers to a file.

Note: The user will still be able to drop a folder onto your *Workflow* in *DropPy*, it will just **silently be filtered out**.

## Arguments

None.

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Filter.OnlyFiles/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- The *Task* [Filter.OnlyDirectories]({{<ref "filter-only-directories.md">}}) is very similar to this one
