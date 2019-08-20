---
title: "Markdown.FromHtml"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* creates **Markdown** output from **HTML** input.

Internally **Markdown.FromHtml** relies on the *html2text* package.

{{% alert theme="danger" %}}The **html2text** package is **not** part of Python's standard library and needs to be installed beforehand.{{% /alert %}}

## Arguments

None.

## Requirements

#### Python (Non-Standard-Library Packages)

- html2text
    - Run the following command in your Terminal: `sudo pip install html2text`.
    - If this worked you’re already done. If you get an error [install pip]({{<ref "pip.md">}}) first.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Markdown.FromHtml/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://pypi.python.org/pypi/html2text" target="_blank">html2text on pypi.python.org {{%icon fa-external-link-square%}}</a>
- <a href="https://github.com/Alir3z4/html2text/" target="_blank">html2text on GitHub {{%icon fa-external-link-square%}}</a>
