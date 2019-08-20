---
title: "Image.Ocr"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes images and runs them through the **Tesseract** engine for **OCR** (*optical character recognition*). You'll get a text file containing the results.

**Image.Rotate** works with the PIL/pillow package internally and supports about <a href="http://pillow.readthedocs.io/en/stable/handbook/image-file-formats.html" target="_blank">30 different file formats {{%icon fa-external-link-square%}}</a> for input and output.

{{% alert theme="danger" %}}The **PIL/pillow** package is **not** part of Python's standard library and <a href="https://docs.droppy.eberl.se/articles/pil-pillow/">needs to be installed</a> beforehand.{{% /alert %}}

{{% alert theme="danger" %}}The **pytesseract** package is **not** part of Python's standard library and <a href="https://docs.droppy.eberl.se/articles/tesseract/">needs to be installed</a> beforehand.{{% /alert %}}

{{% alert theme="danger" %}}The **Tesseract** external executable is **not** part of macOS and <a href="https://docs.droppy.eberl.se/articles/tesseract/">needs to be installed</a> beforehand.{{% /alert %}}

## Arguments

- **tesseract_executable** (optional) is a *string* of the full path to your tesseract binary.

```python
# tesseract_executable = '/usr/local/bin/tesseract'  # default
tesseract_executable = '/my/non-default/tesseract'
```

- **language** (optional) is a *string* of the <a href="https://www.macports.org/ports.php?by=name&substr=tesseract-" target="_blank">language code {{%icon fa-external-link-square%}}</a> to use for text recognition.

```python
# language = 'eng'  # default
language = 'deu'
```

- **boxes** (optional) is a *boolean* that determines if `batch.nochop makebox` gets added to the Tesseract call. May provide better results in some cases.

```python
# boxes = False  # default
boxes = True
```

- **config** (optional) is a *string* containing other <a href="https://github.com/tesseract-ocr/tesseract/wiki/Command-Line-Usage" target="_blank">Tesseract parameters {{%icon fa-external-link-square%}}</a>.

```python
# config = ''  # default
config = '--tessdata-dir "/my/special/tessdata"'
```

## Requirements

#### Python (Non-Standard-Library Packages)

- PIL/pillow ([installation instructions]({{<ref "pil-pillow.md">}}))
- pytesseract ([installation instructions]({{<ref "tesseract.md">}}))

#### External Executables

- Tesseract ([installation instructions]({{<ref "tesseract.md">}}))

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Image.Ocr/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://www.macports.org/ports.php?by=name&substr=tesseract-" target="_blank">List of Tesseract language codes {{%icon fa-external-link-square%}}</a>
- <a href="https://github.com/tesseract-ocr/tesseract/wiki/Command-Line-Usage" target="_blank">Tesseract parameters {{%icon fa-external-link-square%}}</a>
