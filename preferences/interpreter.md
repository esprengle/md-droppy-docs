# Interpreter

<img src="/images/preferences-interpreter-screenshot.png" alt="Interpreter screenshot" style="display:block; max-width:846px; max-height:478px; width:100%; height:auto;">

## Add

You can add any number of [interpreters]({{< ref "macos-python.md" >}}) or [virtual environments]({{< ref "virtual-env.md" >}}).

When creating a new one, the defaults are:

- The **Name** *New Interpreter*.
- The **Executable** of *macOS' pre-installed* Python interpreter at `/usr/bin/python`.
- The **Arguments** `-B`. This prevents `*.pyc` and `*.pyo` files from being created on execution.

## Edit

You can edit the **Name** of your new interpreter in the list on the left side. The **Name** you enter here corresponds to the attribute `interpreterName` in *Workflow* `*.json` files.

Some restrictions apply:

- The interpreter's **Name** must be unique.
- The path to the **Executable** must be valid.
- The path to the **Executable** has to point to a file with the name `python`, `python2` or `python3`.
- Arguments have to go into the **Arguments** text field, not into the **Executable** one. 
- The *macOS pre-installed* interpreter can't be edited.

## Remove

All [interpreters]({{< ref "macos-python.md" >}}) or [virtual environments]({{< ref "virtual-env.md" >}}) that you added yourself can be removed.

The *macOS pre-installed* interpreter can't be removed.

## Information

*Version* runs `{your-python-interpreter-path} --version`, parses and displays the result.

*System default* compares the result of `which python` with the path of your interpreter.

*Virtual environment* checks if the path to your interpreter constitues a [virtual environment]({{< ref "virtual-env.md" >}}) or not.
