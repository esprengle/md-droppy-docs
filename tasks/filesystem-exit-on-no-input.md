---
title: "FileSystem.ExitOnNoInput"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* makes sure there are files or folders in its input_dir. If there's no input availabe it throws an error. All *Tasks* behind it will not run in this case.

**FileSystem.ExitOnNoInput** also passes its input to its output directory as it is, so you can put another *Task* behind it.

## Arguments

None

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/FileSystem.ExitOnNoInput/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
