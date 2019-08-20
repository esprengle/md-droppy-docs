# Virtual Environments

## What is a Virtual Environment?

When you install a 3rd party package with `pip` it's put in your Python interpreter's `site-packages` directory. From that moment on it is available for all scripts that you run through this interpreter.

Using *Virtual Environments* avoids having to install all 3rd party packages globally.

This keeps dependencies required by different projects in separate places. And solves the *"Project X depends on version 1.x but Project Y needs 4.x"* dilemma without repeatedly re-installing this package.

You also have more overview about what non-default packages (and what versions) your scripts require. This is especially helpful when sharing your scripts with other people.

## What does that mean for me?

If **you just use the Python standard library** you don't need a *Virtual Environment*.

If **you only use the current release** of some 3rd party Python package and there's no big reason why this package should not be installed into your `site-packages` directory. Sure it's a bit cleaner but using a *Virtual Environment* is no must.

If **you plan on sharing your script with other people** using a *Virtual Environment* is a great way to automatically get a correct `requirements.txt` file describing what your script needs.

If you **need to use one specific version** of a Python package (for example an older one, a patched one, a specific fork, or a beta) you save yourself much trouble by creating a *Virtual Environment* for it.

## Creating virtual environments

### Python 2

The package `virtualenv` (<a href="https://pypi.python.org/pypi/virtualenv" target="_blank">pypi {{%icon fa-external-link-square%}}</a>) is not part of Python's standard library. You'll have to install it manually:

    pip install virtualenv

Updating:

    pip install --upgrade virtualenv

Checking version:

    virtualenv --version

Creating a new *Virtual Environment*:

    virtualenv "/path/to/the/directory/of/my_sample_env_1"

If both Python 2 and Python 3 are present on the system, you have to specify the path to the Python to use when creating a *Virtual Environment*. Just running `python` may default to use Python 3, check by running `which python`.

    virtualenv -p "/usr/bin/python" "/path/to/the/directory/of/my_sample_env_1"

Running `virtualenv` with the option `--no-site-packages` will exclude all packages that are installed globally. This can be useful for keeping the package list clean and correct in case it needs to be distributed later. 

Once `virtualenv` has run, you will see some new directories inside the directory you supplied. To activate your *Virtual Environment* you need to run the `activate` script in the **bin subdirectory**:

    cd "/path/to/the/directory/of/my_sample_env_1/bin"

    . activate

With this, you are now ready to install your project-specific packages using `pip`, which will then reside in the **lib subdirectory**:

    pip install openpyxl

Later you can deactivate your *Virtual Environment* in the shell again:

    cd "/path/to/the/directory/of/my_sample_env_1/bin"

    . deactivate

### Python 3

Although you could also install and use `virtualenv` (<a href="https://pypi.python.org/pypi/virtualenv" target="_blank">pypi {{%icon fa-external-link-square%}}</a>) with Python 3 it is recommended to use `venv` (<a href="https://docs.python.org/3/library/venv.html" target="_blank">documentation {{%icon fa-external-link-square%}}</a>) instead.

Since Python 3.3 `venv` is part of the standard library, no need to install anything.

*"`venv` by nature of being part of Python itself has access to the internals of Python which means it can do things the right way with far fewer hacks. `venv` can be thought of virtualenv done right, with the blessing and support of the Python developers."* (<a href="https://www.reddit.com/r/learnpython/comments/4hsudz/pyvenv_vs_virtualenv/" target="_blank">Source {{%icon fa-external-link-square%}}</a>)

Creating a new *Virtual Environment*:

    python3 -m venv "/path/to/the/directory/of/my_sample_env_2"

Once `venv` has run, you will see some new directories inside the directory you supplied. To activate your *Virtual Environment* you need to run the `activate` script in the **bin subdirectory**:

    cd "/path/to/the/directory/of/my_sample_env_2/bin"

    . activate

With this, you are now ready to install your project-specific packages using `pip`, which will then reside in the **lib subdirectory**:

    pip install openpyxl

Later you can deactivate your *Virtual Environment* in the shell again:

    cd "/path/to/the/directory/of/my_sample_env_2/bin"

    . deactivate

## Using Pip with Virtual Environments

{{% alert theme="danger" %}}Run these commands while a *Virtal Environment* is active. Otherwise pip lists/freezes/lists globally.{{% /alert %}}

- `pip list` outputs a human readable list of all your installed packages.

- `pip freeze > requirements.txt` will create a requirements.txt file, which contains a list of all the packages in the current environment, and their respective versions.

- `pip install -r requirements.txt` installs all the packages specified in the file. Run it re-create an existing environment.

## One more tip

Remember to exclude all *Virtual Environment* directories from source control by adding it to the ignore list.

Instead make sure to commit your `requirements.txt` file.

## Implications for DropPy

You can set any number of [interpreters]({{< ref "macos-python.md" >}}) and *Virtual Environments* in **Preferences** - **Interpreter**. See the [documentation]({{< ref "interpreter.md" >}}) for details.
