---
title: "Image.Resize"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes images and resizes them.

**Image.Resize** works with the PIL/pillow package internally and supports about <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">30 different file formats {{%icon fa-external-link-square%}}</a> for input and output.

{{% alert theme="danger" %}}The **PIL/pillow** package is **not** part of Python's standard library and <a href="https://docs.droppy.eberl.se/articles/pil-pillow/">needs to be installed</a> beforehand.{{% /alert %}}

## Arguments

- **width** (optional) is an *integer* that specifies the horizontal size of the target image in pixels.

```python
# width = 800  # default
width = 1920
```

- **height** (optional) is an *integer* that specifies the vertical size of the target image in pixels.

```python
# height = 600  # default
height = 1080
```

- **filter** (optional) is a *string* that determines which algorithm should be used for the transformation. The options are `antialias` (=Lanczos), `box`, `bilinear`, `hamming`, `bicubic` and `nearest`.
    - `antialias` looks best but has the worst performance.
    - `nearest` looks worst but has the best performance.

```python
# filter = 'antialias'  # default 
filter = 'nearest'
```

## Requirements

#### Python (Non-Standard-Library Packages)

- PIL/pillow ([installation instructions]({{<ref "pil-pillow.md">}}))

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Image.Resize/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="http://python-pillow.org" target="_blank">Pillow main site {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/" target="_blank">Pillow documentation {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">Pillow documentation - supported file formats {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/reference/Image.html?highlight=rotate#PIL.Image.Image.resize" target="_blank">Pillow documentation - resize function {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/handbook/concepts.html#filters" target="_blank">Pillow documentation - filter quality and performance {{%icon fa-external-link-square%}}</a>
