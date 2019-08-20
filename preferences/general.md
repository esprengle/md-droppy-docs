# General

<img src="/images/preferences-general-screenshot.png" alt="General screenshot" style="display:block; max-width:846px; max-height:328px; width:100%; height:auto;">

## Development mode

*Enabling* development mode has the following effects:

- All intermediary files in *DropPy*'s *temp directory* will be deleted when exiting the application, not right away.

- A small **tmp** button appears in the bottom right of the main window. Clicking it opens *DropPy*'s *temp directory*.

- After running a *Workflow* two more buttons will show up in the main window to help with debugging:
    - **re-drop** runs the Workflow on the elements you just dropped again.
    - **log** opens the `droppy.log` file in the macOS Console application.

In contrast *disabling* development mode has these effects:

- All intermediary files in *DropPy*'s *temp directory* are **deleted automatically after successful execution** of the *Workflow*. If an **error occurs during execution they are left untouched** for now and deleted when exiting the application.

- You will not be shown the debugging buttons after running a *Workflow*.

The default setting is *disabled*.

Development mode can also be toggled quickly through the *Workflow* menu and the keyboard shortcut `⌘` + `d`.

## Update check

Choose how often *DropPy* should automatically check for updates:

- Never
- Every day
- Every week (default)
- Every month

The check is performed when starting the application.

Regardless of the setting here it's always possible to check for updates from the **menu**.
