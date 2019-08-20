# Creating a Workflow

## 1. Create a json file

Create a new file `*.json` the **Workflows** subfolder of your *DropPy workspace* (default: `/Users/YourUserName/DropPy/Workflows/`).

The *Workflows* that come with *DropPy* adhere to a naming scheme of **Category.Name** - but you can name your *Workflow* as you wish.

## 2. Specify name and interpreter

Take a look into the *Workflows* that come with *DropPy* for the structure of *Workflow* json files.

The following information is required:

```python
{
  "name": "Audio flac to mp3 iTunes",
  "interpreterName": "macOS pre-installed",
  ...
}
```

- **name** is a string specifying the name of this *Workflow* in the dropdown menu. It has to be unique, otherwise you'll get alerted.
- **interpreterName** is a string stating which of your interpreters in Preferences - Interpreters this *Workflow* should use. The default value is `macOS pre-installed`. You will be alerted if an interpreter with that name is not found.

The rest of the attributes is optional:
```python
{
  ...
  "author": "guenther@eberl.se",
  "description": "Convert any dropped FLAC file to an mp3 and import it into iTunes.",
  "documentation": "https://github.com/geberl/swift-droppy/workflows/audio-flac-to-mp3-itunes",
  "image": "flac.png",
  ...
}
```

- **author** is a string of the name or email of the author of that *Workflow*. This info is not used yet in the user interface.
- **description** is a string stating what this *Workflow* does. This info is not used yet in the user interface.
- **documentation** is a string of the URL where some docs concerning that *Workflow* can be found. This info is not used yet in the user interface.
- **image** is a string of the filename of the image to use on the drag & drop area. Images are searched in the **Images** subfolder of your *DropPy workspace* (default: `/Users/YourUserName/DropPy/Images/`). A default image is used when nothing is specified (or the specified image is not found).

## 3. Specify the Tasks to run

Next come the *Tasks* in the order they should be executed in along with their keyword arguments:

```python
{
  ...
  "queue": [
    {
      "task": "Filter.ByUTIs",
      "kwargs":
      {
        "utis": ["files"]
      }
    },
    {
      "task": "FileSystem.ExitOnNoInput"
    },
    ...
  ]
}
```

- **queue** (required) is the element that wraps everything.
- **task** (required) is a string identical to the folder name in the **Tasks** subfolder of your *DropPy workspace* (default: `/Users/YourUserName/DropPy/Tasks/`)
- **kwargs** (optional) is a dictionary of key-value pairs that will be passed through to the *Task* when it's called.
