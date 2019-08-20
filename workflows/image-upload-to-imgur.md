---
title: "Image upload to Imgur"
description: ""
date: "2017-12-13T10:00:00+02:00"
draft: false
---

## Details

Upload an image to the popular image hosting service <a href="https://imgur.com" target="_blank">imgur.com {{%icon fa-external-link-square%}}</a>.

{{% alert theme="danger" %}}You need an **Imgur API Key** for this to work. Edit the `client_id` argument in the *Workflow*. More info in the documentation of the *Task* <a href="https://docs.droppy.eberl.se/tasks/web-imgur-upload/">Web.ImgurUpload</a>.{{% /alert %}}

## Tasks

- [Filter.ByUTIs]({{<ref "filter-by-utis.md">}})
- [FileSystem.ExitOnNoInput]({{<ref "filesystem-exit-on-no-input.md">}})
- [Filter.ByExtensions]({{<ref "filter-by-extensions.md">}})
- [FileSystem.ExitOnNoInput]({{<ref "filesystem-exit-on-no-input.md">}})
- [Web.ImgurUpload]({{<ref "web-imgur-upload.md">}})
- [MacOS.OpenFilesInApp]({{<ref "macos-open-files-in-app.md">}})

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Workflows/image_upload_to_imgur.json" target="_blank">Code of Workflow on GitHub {{%icon fa-external-link-square%}}</a>
