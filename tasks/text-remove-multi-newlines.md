---
title: "Text.RemoveMultiNewlines"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* parses a textfile and removes multiple line breaks that follow each other. One empty line is ok, but two are not - and get reduced to one.

**Text.RemoveMultiNewlines** can be used with any kind of text file (markdown, csv, log).

Internally it does **not** rely on **Regular Expressions** but iterates over the lines and checks them via `if len(line.strip()) == 0`.

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

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Text.RemoveMultiNewlines/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
