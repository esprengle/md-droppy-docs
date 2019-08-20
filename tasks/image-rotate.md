---
title: "Image.Rotate"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes images and rotates them.

**Image.Rotate** works with the PIL/pillow package internally and supports about <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">30 different file formats {{%icon fa-external-link-square%}}</a> for input and output.

{{% alert theme="danger" %}}The **PIL/pillow** package is **not** part of Python's standard library and <a href="https://docs.droppy.eberl.se/articles/pil-pillow/">needs to be installed</a> beforehand.{{% /alert %}}

Note: Rotation of lossy formats (like JPEG) is not lossless. Image quality degrades.

## Arguments

- **degrees** (optional) is a *float* that describes the direction and magnitude of the rotation. Positive is counter-clockwise, negative is clockwise.

```python
# degrees = 90.0  # default
degrees = -45.0
```

- **expand** (optional) is a *boolean* that determines what should happen to the base area of the image if a value other than multiples of 90 are passed as **degrees**. *True* expands the base area with a black background, *False* makes the output the same size as the input and cuts off parts of the image.

```python
# expand = True  # default
expand = False
```

## Requirements

#### Python (Non-Standard-Library Packages)

- PIL/pillow ([installation instructions]({{<ref "pil-pillow.md">}}))

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Image.Rotate/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://python-pillow.org" target="_blank">Pillow main site {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/" target="_blank">Pillow documentation {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">Pillow documentation - supported file formats {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/reference/Image.html?highlight=rotate#PIL.Image.Image.rotate" target="_blank">Pillow documentation - rotate function {{%icon fa-external-link-square%}}</a>