# Python on macOS

## Pre-installed Versions

### Python 2

At least since **Mac OS X Tiger** a *somewhat recent* version of **Python 2** comes pre-installed. Older versions of Python may also be included for compatibility reasons.

macOS Version | macOS Release Date | Python Version | Python Release Date
--- | --- | --- | ---
10.3 Panther | 2003-10-24 | ? | ?
10.4 Tiger | 2005-04-29 | 2.3.5 | 2005-02-08
10.5 Leopard | 2007-10-26 | 2.5.1 | 2007-04-19
10.6 Snow Leopard | 2009-08-28 | 2.6.1 | 2008-12-04
10.7 Lion | 2011-07-20 | 2.7.1 | 2010-11-27
10.8 Mountain Lion | 2012-07-25 | 2.7.2 | 2011-06-11
10.9 Mavericks | 2013-10-22 | 2.7.5 | 2013-05-12
10.10 Yosemite | 2014-10-16 | 2.7.6 | 2013-11-10
10.11 El Capitan | 2015-09-30 | 2.7.10 | 2015-05-23
10.12 Sierra | 2016-09-20 | 2.7.10 | 2015-05-23
10.13 High Sierra | 2017-09-25 | 2.7.10 | 2015-05-23
10.14 Mojave | 2018-09-24 | 2.7.10 | 2015-05-23

The path is always `/System/Library/Frameworks/Python.framework/Versions/{version-number}` with a symlink to the latest included version at `/usr/bin/python`.

The package manager `pip` is not included but `easy_install` is. You can install `pip` by running `sudo easy_install pip`.

### Python 3

Until now **Python 3** did never come pre-installed.

## Distributions

The *current stable versions* are **Python 2.7.15** and **Python 3.7.2**.

To use these versions on your Mac there are several popular options. For a full cross-platform overview see <a href="https://www.python.org/download/alternatives/" target="_blank">Alternative Python Implementations {{%icon fa-external-link-square%}}</a>.

### Python.org

The official CPython implementation is available at <a href="https://python.org" target="_blank">Python.org {{%icon fa-external-link-square%}}</a>.

Download the *MacOS X64-bit/32-bit Installer* and run the `*.pkg` file.

This does not overwrite the Python 2 version that comes pre-installed in macOS. Instead it installs Python into `/Library/Frameworks/Python.framework/Versions/{version-number}`.

Symlinks are created at `/usr/local/bin/python` and `/usr/local/bin/python3`.

### Homebrew

<a href="https://brew.sh" target="_blank">Homebrew {{%icon fa-external-link-square%}}</a> is a package manager for macOS. Much like **apt** on Ubuntu/Debian or **pacman** on Arch.

It does not come with macOS but needs to be installed beforehand. The `sudo` password is needed during installation and the **Command line tools for Xcode** will be installed alongside:

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

Once installed you can use it go get the latest stable version of Python 2:

    brew install python

And Python 3:

    brew install python3

This does not overwrite the Python 2 version bundled with macOS. Instead it installs Python 2 into `/usr/local/Cellar/python/{version-number}` and Python 3 into `/usr/local/Cellar/python3/{version-number}`. 

Symlinks are created at `/usr/local/bin/python2` and `/usr/local/bin/python3`.

Another benefit of using a package manager is easy updating. For Python 2:

    brew upgrade python

And Python 3:

    brew upgrade python3

### MacPorts

Another package manager is <a href="https://www.macports.org/" target="_blank">MacPorts {{%icon fa-external-link-square%}}</a>.

The command to install Python 2 is:

    sudo port install python27

And Python 3:

    sudo port install python36

Again your existing Python installations are not overwritten. The path used is `/opt/local/Library/Frameworks/Python.framework/Versions/{version-number}`.

### Pypy

<a href="http://pypy.org/download.html" target="_blank">Pypy {{%icon fa-external-link-square%}}</a> is the Python interpreter written in Python itself.

It tends to run very fast and <a href="http://speed.pypy.org" target="_blank">beats CPython in most benchmarks {{%icon fa-external-link-square%}}</a> - however the first execution takes a bit longer.

### Anaconda & Miniconda

If you are into *data science* you should look into <a href="https://www.continuum.io/downloads" target="_blank">Anaconda {{%icon fa-external-link-square%}}</a>. Since there are a lot of packages included that installer is substantially larger than the previous options (450mb vs 30mb).

<a href="https://conda.io/miniconda.html"  target="_blank">Miniconda {{%icon fa-external-link-square%}}</a> just provides Python, the package manager **conda**, and a minimal set of packages.

Under the hood Anaconda/Miniconda are repackaged versions of CPython.

## Implications for DropPy

The pre-installed version of Python 2 is enough for starting out.

If you still wonder **what version to get** or if you **need Python 3** just install the latest one from <a href="https://python.org/" target="_blank">Python.org {{%icon fa-external-link-square%}}</a>. That is unless you already have Homebrew/Macports, then get it from there.

You can set any number of interpreters and [virtual environments]({{< ref "virtual-env.md" >}}) in **Preferences** - **Interpreter**. See the [documentation]({{< ref "interpreter.md" >}}) for details.
