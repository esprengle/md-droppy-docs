# Calibre.Convert

## Description

This *Task* converts **text documents** between a multitude of different file formats: *azw*, *azw3*, *azw4*, *cbz*, *cbr*, *cbc*, *chm*, *djvu*, *docx*, *epub*, *fb2*, *html*, *htmlz*, *lit*, *lrf*, *mobi*, *odt*, *pdf*, *prc*, *pdb*, *pml*, *rb*, *rtf*, *snb*, *tcr*, *txt* and *txtz*.

As its name suggests **Calibre.Convert** works with the open-source ebook management program <a href="https://calibre-ebook.com" target="_blank">Calibre {{%icon fa-external-link-square%}}</a> under the hood.

{{% alert theme="danger" %}}The **Calibre** external executable is **not** part of macOS and needs to be installed beforehand.{{% /alert %}}

## Arguments

- **ebookconvert_executable** (optional) is a *string* of the full path to your ebook-convert binary.

```python
# ebookconvert_executable = '/Applications/calibre.app/Contents/MacOS/ebook-convert'  # default
ebookconvert_executable = '/my/non-default/ebook-convert'
```

- **extension** (optional) is a *string* specifying your desired output format. Has to be one of the above list. Do not prefix a dot.

```python
# extension = 'mobi'  # default
extension = 'epub'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

- Calibre (<a href="https://calibre-ebook.com" target="_blank">download {{%icon fa-external-link-square%}}</a>)

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Calibre.Convert/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://manual.calibre-ebook.com/conversion.html" target="blank">Calibre conversion system documentation {{%icon fa-external-link-square%}}</a>
