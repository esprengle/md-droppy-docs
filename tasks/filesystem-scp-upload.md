---
title: "FileSystem.ScpUpload"
description: ""
date: "2017-12-13T15:30:00+02:00"
draft: false
---

## Description

This *Task* takes files and folders and uploads them to a server using **SCP**.

**FileSystem.ScpUpload** also passes its input to its output directory as it is, so you can put another *Task* behind it.

Note: For security reasons only **key-based authentication** is supported. Using a username/password combination is not possible on purpose. You do not want your *Workflows* to contain passwords in plain text.

## Arguments

- **server_address** (required) is a *string* of the IP address or host that you want to connect to.

```python
server_address = '192.168.1.123'
```

- **remote_path** (required) is a *string* specifying the full path where to upload your files to on the server.

```python
remote_path = '/home/john/uploads'
```

- **username** (required) is a *string* specifying your remote user name.

```python
username = 'john'
```

- **scp_executable** (optional) is a *string* specifying the full path to the scp binary.

```python
# scp_executable = '/usr/bin/scp'  # default
scp_executable = '/my/non-default/scp'
```

## Requirements

#### Python (Non-Standard-Library Packages)

None.

#### External Executables

None.

#### API Credentials

None.

## Resources

- <a href="https://github.com/geberl/droppy-workspace/blob/master/Tasks/FileSystem.ScpUpload/task.py" target="_blank">Code of Task on GitHub {{%icon fa-external-link-square%}}</a>
- <a href="https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server" target="_blank">Tutorial on how to configure SSH Key-Based Authentication on a Linux Server {{%icon fa-external-link-square%}}</a>
