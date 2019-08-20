# Tesseract

**Tesseract** is an open source engine for **OCR** (*optical character recognition*), originally developed at HP and now at Google.

**pytesseract** is a Python package that acts as a wrapper.

Neither comes with macOS by default.

## Errors

If the `tesseract` executable or the `pytesseract` Python package are not installed and you are running a *Task* that requires it, *DropPy* will show an error:

<img src="/images/error-droppy.png" alt="Error DropPy Alert screenshot" style="display:block; height:auto;">

And the **log file** will show this (`tesseract` executable missing):

<img src="/images/error-tesseract.png" alt="Error Logfile tesseract screenshot" style="display:block; height:auto;">

Or this (`pytesseract` Python package missing):

<img src="/images/error-pytesseract.png" alt="Error Logfile pytesseract screenshot" style="display:block; height:auto;">

Install `tesseract` and `pytesseract` to get the *Task* working.

## Installation

### tesseract

```bash
brew install tesseract
```

If this worked you’re already done. If you get an error <a href="https://docs.droppy.eberl.se/articles/macos-python/#homebrew">install homebrew</a> first.

### pytesseract

```bash
sudo pip install pytesseract
```

If this worked you’re already done. If you get an error [install pip]({{<ref "pip.md">}}) first.

## Resources

- <a href="https://github.com/tesseract-ocr/tesseract" target="_blank">The Tesseract project on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://github.com/tesseract-ocr/tesseract/wiki" target="_blank">Tesseract wiki page on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://www.pyimagesearch.com/2017/07/10/using-tesseract-ocr-python/" target="_blank">Improving results with some image preprocessing {{%icon fa-external-link-square%}}</a>
- <a href="https://github.com/madmaze/pytesseract" target="_blank">The pytesseract project on GitHub {{%icon fa-external-link-square%}}</a>
