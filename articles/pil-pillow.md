# PIL/Pillow

**PIL** is the Python Image Library. It was deprecated some time ago and **Pillow** is the successor. Neither package is part of Python's standard library.

## Errors

If `pillow` is not installed and you are running a *Task* that requires it, *DropPy* will show an error:

<img src="/images/error-droppy.png" alt="Error DropPy Alert screenshot" style="display:block; height:auto;">

And the **log file** will show this:

<img src="/images/error-pil.png" alt="Error Logfile PIL screenshot" style="display:block; height:auto;">

Install the `pillow` Python package to get the *Task* working.

## Installation

Since `pillow` is a very common package and therefor useful to have available globally we use `sudo` for installation. Run the following command in your *Terminal*:

```bash
sudo pip install pillow
```

If this worked you’re already done. If you get an error [install pip]({{<ref "pip.md">}}) first.

## Checking if PIL/pillow works

In a shell the following command should **run without displaying an error**:

```bash
python -c "from PIL import Image"
```

**If you get no output everything is ok.**

If you get the following output `pillow` is not installed:

```python
Traceback (most recent call last):
  File "<string>", line 1, in <module>
ImportError: No module named PIL
```

## Uninstallation

Just for the sake of completeness.

`pillow` (and its dependency `olefile`) can again be removed with:

```bash
sudo pip uninstall pillow olefile
```

## Resources

- <a href="http://python-pillow.org" target="_blank">Pillow main site {{%icon fa-external-link-square%}}</a>
- <a href="http://pillow.readthedocs.io/en/stable/" target="_blank">Pillow documentation {{%icon fa-external-link-square%}}</a>
- <a href="https://pypi.python.org/pypi/Pillow/4.3.0" target="_blank">Pillow on pypi.python.org {{%icon fa-external-link-square%}}</a>
