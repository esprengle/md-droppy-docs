---
title: "Image.Convert"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes images and converts them to a different format.

**Image.Convert** works with the PIL/pillow package internally and supports about <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">30 different file formats {{%icon fa-external-link-square%}}</a> for input and output.

{{% alert theme="danger" %}}The **PIL/pillow** package is **not** part of Python's standard library and <a href="https://docs.droppy.eberl.se/articles/pil-pillow/">needs to be installed</a> beforehand.{{% /alert %}}

## Arguments

- **extension** (optional) is a *string* that contains the extension of the target format. Do not pass a preceding dot.

```python
# extension = 'png'  # default
extension = 'jpg'
```

- **background** (optional) is a *list* of *integers* that represent the RGB color to use as replacement for transparency. This is only used when you convert an input file that has an alpha channel (like a png with transparent background) to an *extension* doesn't support transparency (like jpg).

```python
# background = [255, 255, 255]  # default
background = [0, 0, 0]
```

## Requirements

#### Python (Non-Standard-Library Packages)

- PIL/pillow ([installation instructions]({{<ref "pil-pillow.md">}}))

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Image.Convert/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://python-pillow.org" target="_blank">Pillow main site {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/" target="_blank">Pillow documentation {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">Pillow documentation - supported file formats {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/reference/Image.html?highlight=rotate#PIL.Image.Image.save" target="_blank">Pillow documentation - save function {{%icon fa-external-link-square%}}</a>
