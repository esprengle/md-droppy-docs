---
title: "Web.YouTubeDownload"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* downloads **individual videos** or **complete playlists** from **YouTube** and <a href="https://rg3.github.io/youtube-dl/supportedsites.html" target="_blank">a lot of other {{%icon fa-external-link-square%}}</a> sites.

**Web.YouTubeDownload** works with the open-source program <a href="https://github.com/rg3/youtube-dl/" target="_blank">youtube-dl {{%icon fa-external-link-square%}}</a> under the hood.

{{% alert theme="danger" %}}The **youtube-dl** external executable is **not** part of macOS and <a href="https://docs.droppy.eberl.se/articles/tools-audio-video/">needs to be installed</a> beforehand.{{% /alert %}}

## Arguments

- **youtubedl_executable** (optional) is a *string* of the full path to your youtube-dl binary.

```python
# youtubedl_executable = '/usr/local/bin/youtube-dl'  # default
youtubedl_executable = '/my/non-default/youtube-dl'
```

- **output_file_pattern** (optional) is a *string* specifying how your downloaded files should be named. See the <a href="http://manpages.ubuntu.com/manpages/precise/man1/youtube-dl.1.html#contenttoc4" target="_blank">documentation of output template names {{%icon fa-external-link-square%}}</a> for what metadata is accessible.

```python
# output_file_pattern = '%(title)s.%(ext)s'  # default
output_file_pattern = '%(id)s - %(uploader)s - %(title)s.%(ext)s'
```

- **other_args** (optional) is a *string* containing other <a href="https://linux.die.net/man/1/ffmpeg" target="_blank">youtube-dl parameters  {{%icon fa-external-link-square%}}</a>.

```python
# other_args = ''  # default
other_args = '-padleft 10 -padright 10'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

- youtube-dl ([installation instructions]({{<ref "tools-audio-video.md">}}))

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Web.YouTubeDownload/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://github.com/rg3/youtube-dl/" target="_blank">youtube-dl project on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://rg3.github.io/youtube-dl/supportedsites.html" target="_blank">youtube-dl supported sites {{%icon fa-external-link-square%}}</a>
- <a href="http://manpages.ubuntu.com/manpages/precise/man1/youtube-dl.1.html" target="_blank">youtube-dl man page {{%icon fa-external-link-square%}}</a>
