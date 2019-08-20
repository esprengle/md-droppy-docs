# Editor

<img src="/images/preferences-editor-screenshot.png" alt="Editor screenshot" style="display:block; max-width:846px; max-height:363px; width:100%; height:auto;">

## External text editor

DropPy allows you to use your favorite text editor when working on *Workflows*. Just drag & drop the `*.app` from **Finder** into the gray box.

Verified working:

- <a href="https://atom.io" target="_blank">Atom {{%icon fa-external-link-square%}}</a> v1.21
- <a href="http://www.barebones.com/products/bbedit/" target="_blank">BBEdit {{%icon fa-external-link-square%}}</a> v11.6
- <a href="http://macvim-dev.github.io/macvim/" target="_blank">MacVim {{%icon fa-external-link-square%}}</a> v8.0
- <a href="https://neovim.io" target="_blank">NeoVim {{%icon fa-external-link-square%}}</a> v0.2 (if <a href="https://github.com/rogual/neovim-dot-app" target="_blank">installed as an app {{%icon fa-external-link-square%}}</a>)
- <a href="http://www.sublimetext.com" target="_blank">Sublime Text {{%icon fa-external-link-square%}}</a> Build 3134
- <a href="https://www.textasticapp.com/mac.html" target="_blank">Textastic {{%icon fa-external-link-square%}}</a> v3.2
- <a href="https://code.visualstudio.com" target="_blank">Visual Studio Code {{%icon fa-external-link-square%}}</a> v1.17

Problematic:

- TextEdit (comes with macOS) v1.12: Messes up the double-quotes in `*.json` files

## Editor for Workflows

Here you can select how you want to edit the `*.json` files that describe what the *Workflow* does.

The editor set here is opened when clicking the *"Edit Workflow"* button on the **main window**.

Your options are:

- Use the **Internal text editor** *(default)*
    - A very basic text editor will open in a new window.
    - This is mostly provided as a fallback.
- Use an **External text editor**
    - This will open the `*.json` file in the external application you selected above.
    - This is the recommended option.
