# Requirements

## macOS

To run *DropPy* you need a Mac running at least **macOS 10.12 Sierra**. Apple's latest version **macOS 10.13 High Sierra** is fully supported.

Running *DropPy* on prior versions of macOS is not possible. ([why?]({{< ref "faq.md" >}}))

## Python

**Sierra** and **High Sierra** already come with **Python 2.7** pre-installed.

There is no need to download another Python interpreter - but you can of course do this. *DropPy* supports multiple Interpreters ([more info]({{< ref "interpreter.md" >}})).

## Python Packages

Some *Tasks* require **Python packages** that are not included in the **standard library**, for example `PIL` or `requests`.

If a *Workflow* fails take a look in the **log file** to see the **exact error** of the *Task*. Then just refer to <a href="https://docs.droppy.eberl.se/tasks/">its documentation</a>.
