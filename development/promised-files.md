# Promised Files

## What are promised files?

Some apps store data in **internal databases**, **not as files**.

For example *Apple Mail* doesn't store the individual emails as `*.eml` files in `~\Library\Mail\`. Instead you'll find rather big `*.mbox` files there.

So if you use *drag & drop* on an object like this **there is no file that could just be copied** from one location to another. Instead the source application gets notified that you dropped an object (and where), and in turn it *promises* to create a file for it here.

This means **file creation is completely in the hands of the source application**. *DropPy* just tells the app to write its data to `{droppy-tmp-dir}\_cache\0\files.promised\` - and then waits for the app to report it's finished.

## How to work with promised files

Enable [Development Mode](../development-mode.md) and after *drag & drop* check the content of `{droppy-tmp-dir}\_cache\0\` by clicking on the **tmp button**.

If the `files` directory is empty, chances are your expected file is in `files.promised`.

You can also use the *Workflow* [Extract all contained data](../workflows/extract-all-contained-data.md) to get a feeling what data objects contain.
