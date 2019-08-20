# Creating a Task

## 1. Set up the folder structure

Create a new folder in the **Tasks** subfolder of your *DropPy workspace* (default: `/Users/YourUserName/DropPy/Tasks/`).

The *Tasks* that come with *DropPy* adhere to a naming scheme of **Category.Name** - but you can name your *Task* as you wish.

## 2. Create a task.py file

*DropPy* will search for a file named `task.py` in this folder and try to instantiate the **class Task**.

Other `*.py` files can be present and can be imported in your *Task*. *DropPy* will ignore these.

## 3. Write code

Make sure to adhere to the following signature:

```python
class Task(object):
    def __init__(self, input_dir, output_dir, **kwargs):
        # ...
```

- **input_dir** (required) is a *string* of the full path to a directory containing all the input files for this *Task*
    - This is the same directory as the output_dir from the previous *Task* in the *Workflow*
    - This directory can safely be assumed to exist
    - It may however contain 0 files
    - If your *Task* needs files from a different directory ...
        - hardcode that path inside OR
        - traverse the filesystem relative to *input_dir* or *output_dir* OR
        - use *kwargs* to pass a path from the *Workflow*
- **output_dir** (required) is a *string* of the full path to a directory where your *Task* should write its output to
    - If your *Task* has no output you may choose to not write anything here - this however means you can't place another *Task* behind this one
    - This directory can safely be assumed to exist
    - It's empty in the beginning
- **kwargs** (optional) are arbitrary keyword arguments passed from the *Workflow* to your *Task*
    - This is optional, you don't have to implement any keyword arguments
    - See the *Tasks* that come with *DropPy* for examples how to get the values and define defaults

Other than that you're free to do anything in your *Task*. **Just write Python as you're used to!**

## 4. Tips & tricks

If you want to add text to the log file just use `print`:

```python
print('Writing results to "%s"' % directory)
```

If you want to abort and throw an error you can do it like this:

```python
sys.exit('Error message for log file here')
```

Some common helper functions can be found in `/Users/YourUserName/DropPy/Tasks/DropPy.Common/task.py`. Import them like this:

```python
sys.path.append(os.path.abspath(os.path.join(__file__, os.pardir, os.pardir, 'DropPy.Common')))
from file_tools import copy_file, copy_tree
from task_tools import pass_input_to_output
```
