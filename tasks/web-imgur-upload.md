---
title: "Web.ImgurUpload"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes images and uploads them to the popular image hosting service <a href="https://imgur.com" target="_blank">Imgur  {{%icon fa-external-link-square%}}</a>.

**Web.ImgurUpload** uses Imgur's API via the *requests* package.

{{% alert theme="danger" %}}The **requests** package is **not** part of Python's standard library and needs to be installed beforehand.{{% /alert %}}

{{% alert theme="danger" %}}You need an **Imgur API Key** for this *Task* to work. This info is passed as an argument by the *Workflow*.{{% /alert %}}

Note: Your uploads are *anonymous*, they won't shown on your profile/gallery. Instead this *Task* saves the resulting URL to a XML-style **webloc** file in its output directory.

## Arguments

- **client_id** (required) is a *string* that contains your Imgur Client ID.

```python
client_id = 'e613d05c6b46081'  # this id is not live btw
```

## Requirements

#### Python (Non-Standard-Library Packages)

- requests
    - Run the following command in your Terminal: `sudo pip install requests`.
    - If this worked you’re already done. If you get an error [install pip]({{<ref "pip.md">}}) first.

#### External Executables

None.

#### API Credentials

You need to get credentials for Imgur's API:

1. Create an **account** on <a href="https://imgur.com" target="_blank">imgur.com {{%icon fa-external-link-square%}}</a> if you don't already have one

2. Create a **Client ID** and a **Client secret**
    - Login to your **account**
    - Go to <a href="https://api.imgur.com/oauth2/addclient" target="_blank">api.imgur.com/oauth2/addclient  {{%icon fa-external-link-square%}}</a>
    - Enter any name as **Application name**, for example *DropPy Upload*
    - Select **OAuth 2 authorizatio without a callback URL** as authorization type
    - **Application website** can be left blank
    - Enter **your email** in the email field (required)
    - **Description** can be left blank
    - Click **submit**
    - The following page contains your **Client ID** and your **Client secret**
        - Save this info somewhere!
        - The **Client ID** is later also available at <a href="https://imgur.com/account/settings/apps" target="_blank">imgur.com/account/settings/apps  {{%icon fa-external-link-square%}}</a> but the **Client secret** is only shown once
        - The **Client secret**  is not needed for this *Task*, hold on to it anyways so you don't have to reset your token once you need it

3. Edit the *Workflows* that calls this *Task* to pass your `client_id` as an argument.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/Web.ImgurUpload/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://pypi.python.org/pypi/requests" target="_blank">Requests on pypi.python.org {{%icon fa-external-link-square%}}</a>
- <a href="http://docs.python-requests.org/en/master/" target="_blank">Requests project site {{%icon fa-external-link-square%}}</a>
- <a href="https://apidocs.imgur.com" target="_blank">Imgur API documentation {{%icon fa-external-link-square%}}</a>
