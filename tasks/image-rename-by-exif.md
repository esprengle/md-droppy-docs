---
title: "Image.RenameByExif"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes images and renames them according to the date/time info in their **EXIF metadata**.

**Image.RenameByExif** works with the PIL/pillow package internally and supports about <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">30 different file formats {{%icon fa-external-link-square%}}</a> for input and output.

{{% alert theme="danger" %}}The **PIL/pillow** package is **not** part of Python's standard library and <a href="https://docs.droppy.eberl.se/articles/pil-pillow/">needs to be installed</a> beforehand.{{% /alert %}}

Note: Usually only photos taken with your own camera have EXIF tags. Most photos downloaded from the internet have this data already stripped to protect the creator's privacy.

## Arguments

None.

## Requirements

#### Python (Non-Standard-Library Packages)

- PIL/pillow ([installation instructions]({{<ref "pil-pillow.md">}}))

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Image.RenameByExif/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://python-pillow.org" target="_blank">Pillow main site {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/" target="_blank">Pillow documentation {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">Pillow documentation - supported file formats {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/reference/ExifTags.html" target="_blank">Pillow documentation - ExifTags module {{%icon fa-external-link-square%}}</a>
