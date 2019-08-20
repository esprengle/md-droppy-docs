---
title: "Video.Transcode"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* converts **video** (and **audio**) files between a multitude of different file formats.

**Video.Transcode** works with the open-source video recorder/converter <a href="https://ffmpeg.org" target="_blank">FFmpeg {{%icon fa-external-link-square%}}</a> under the hood.

{{% alert theme="danger" %}}The **FFmpeg** external executable is **not** part of macOS and <a href="https://docs.droppy.eberl.se/articles/tools-audio-video/">needs to be installed</a> beforehand.{{% /alert %}}

## Arguments

- **ffmpeg_executable** (optional) is a *string* of the full path to your ffmpeg binary.

```python
# ffmpeg_executable = '/usr/local/bin/ffmpeg'  # default
ffmpeg_executable = '/my/non-default/ffmpeg'
```

- **extension** (optional) is a *string* specifying your desired output format. Do not prefix a dot.

```python
# extension = 'm4v'  # default
extension = '3gp'
```

- **other_args** (optional) is a *string* containing other <a href="https://linux.die.net/man/1/ffmpeg" target="_blank">ffmpeg parameters {{%icon fa-external-link-square%}}</a>.

```python
# other_args = ''  # default
other_args = '-padleft 10 -padright 10'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

- ffmpeg ([installation instructions]({{<ref "tools-audio-video.md">}}))

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Video.Transcode/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://en.wikipedia.org/wiki/FFmpeg" target="_blank">FFmpeg on Wikipedia {{%icon fa-external-link-square%}}</a>
- <a href="https://ffmpeg.org" target="_blank">FFmpeg project site {{%icon fa-external-link-square%}}</a>
- <a href="https://linux.die.net/man/1/ffmpeg" target="_blank">FFmpeg man page {{%icon fa-external-link-square%}}</a>
