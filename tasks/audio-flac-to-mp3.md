# Audio.FlacToMp3

## Description

This *Task* converts audio files from the **lossless flac format** into the **lossy mp3 format**.

**Audio.FlacToMp3** works with the open-source programs <a href="https://xiph.org/flac/" target="_blank">flac {{%icon fa-external-link-square%}}</a> and <a href="http://lame.sourceforge.net" target="_blank">lame {{%icon fa-external-link-square%}}</a> executables under the hood.

{{% alert theme="danger" %}}The **flac** external executables s **not** part of macOS and <a href="https://docs.droppy.eberl.se/articles/tools-audio-video/">needs to be installed</a> beforehand.{{% /alert %}}

{{% alert theme="danger" %}}The **lame** external executable is **not** part of macOS and <a href="https://docs.droppy.eberl.se/articles/tools-audio-video/">needs to be installed</a> beforehand.{{% /alert %}}

## Arguments

- **flac_executable** (optional) is a *string* of the full path to your flac binary.

```python
# flac_executable = '/usr/local/bin/flac'  # default
flac_executable = '/my/non-default/flac'
```

- **lame_executable** (optional) is a *string* of the full path to your lame binary.

```python
# lame_executable = '/usr/local/bin/lame'  # default
lame_executable = '/my/non-default/lame'
```

- **metaflac_executable** (optional) is a *string* of the full path to your metaflac binary.

```python
# metaflac_executable = '/usr/local/bin/metaflac'  # default
metaflac_executable = '/my/non-default/metaflac'
```

- **copy_tags** (optional) is a *boolean* that specifies if metadata should be preserved. Passing *True* makes efforts to copy the popular tags over. If yoiu pass *False* your mp3 file will have no tags.

```python
# copy_tags = False  # default
copy_tags = True
```

- **quality** (optional) is a *string* that specifies the quality setting to use for encoding the files in mp3.

```python
# quality = 'V0'  # default
quality = 'V2'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

- flac (also contains metaflac) ([installation instructions]({{<ref "tools-audio-video.md">}}))
- lame ([installation instructions]({{<ref "tools-audio-video.md">}}))

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Audio.FlacToMp3/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://xiph.org/flac/" target="_blank">Official flac (and metaflac) site {{%icon fa-external-link-square%}}</a>
- <a href="https://xiph.org/flac/documentation_tools_metaflac.html" target="_blank">Metaflac documentation {{%icon fa-external-link-square%}}</a>
- <a href="http://lame.sourceforge.net" target="_blank">Official lame site {{%icon fa-external-link-square%}}</a>
