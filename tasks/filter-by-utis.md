---
title: "Filter.ByUTIs"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

*DropPy* extracts all types of data it finds in your dropped object. In many cases this is more than you want.

Here's where **Filter.ByUTIs** comes in. This *Task* allows you to only continue with certain data types, for example images - but not text.

The way this is achieved is by **passing the desired file's UTIs** (Uniform Type Identifiers) - basically strings that describes the file's content.

To find out what UTIs make sense for your *Workflow* just enable *DropPy*'s [Development Mode]({{<ref "general.md">}}), select the *Workflow* [Extract all contained data]({{<ref "extract-all-contained-data.md">}}), drop your object and look at the resulting timestamped folder in your Downloads directory.

Note: Filtering by extracted data type / UTI is not the same thing as filtering by file extension. Use the *Task* [Filter.ByExtensions]({{<ref "filter-by-extensions.md">}}) for this.

## Arguments

- **utis** (optional) is a *list* of *strings* that contain the UTIs of the files that should get passed on to this *Task*'s output directory. All other files will be not be available for the next *Task*.

```python
# utis = ['files']  # default
utis = ['public.tiff', 'files', 'files.promised']
```

- **flatten_dir** (optional) is a *boolean* that allows control over the directory structure in the *Task's* output directory. If set to `True` all extracted files will be mixed in with each other in the output directory (overwriting may occur!). If set to `False` you get one subdirectory for each UTI.

```python
# flatten_dir = True  # default
flatten_dir = False
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Filter.ByUTIs/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://en.wikipedia.org/wiki/Uniform_Type_Identifier" target="_blank">UTIs on Wikipedia {{%icon fa-external-link-square%}}</a>
- <a href="https://developer.apple.com/library/content/documentation/Miscellaneous/Reference/UTIRef/Articles/System-DeclaredUniformTypeIdentifiers.html#//apple_ref/doc/uid/TP40009259-SW1" target="_blank">List of UTIs from Apple (somewhat outdated, OS X 10.4) {{%icon fa-external-link-square%}}</a>
- <a href="https://developer.apple.com/library/content/documentation/FileManagement/Conceptual/understanding_utis/understand_utis_intro/understand_utis_intro.html" target="_blank">Introduction to Uniform Type Identifiers Overview from Apple {{%icon fa-external-link-square%}}</a>
