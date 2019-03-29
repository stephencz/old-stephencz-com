---
layout: post
title: Recursive FTP Deletion and Transfer with Python
description: A list of everything I've read and what I'm currently reading.
listed: true
was_updated: false
update_date: 
status: finished
categories: [Scripts, Python, Networking]
links: ["Github Repository", "https://github.com/stephencz/scripts", "Full Script", "https://github.com/stephencz/scripts/blob/master/python/site-swap-ftp.py", "FTPLib Documentation", "https://docs.python.org/3/library/ftplib.html"]
---

```python
import ftplib
from ftplib import FTP
from os import listdir
from os.path import isfile, join
```

```python
host = "" #Server IP Address
username = "" #FTP Username
password = "" #FTP Password

whitelist = [".", "..", ".htaccess", ".well-known"] #Files you don't want to delete
blacklist = [] #Files you don't want to upload

server_directory = "" # The directory on the server to recursively delete the contents of. BE CAREFUL WITH THIS. DON'T WIPE YOUR WEBSERVER.
local_directory = "" #The local directory you want to upload the contents of.
```

## Recursive Delete
```python
def recursive_delete(session):
    files = [file for file in session.nlst() if file not in whitelist]

    for file in files:
        try:
            session.delete(file)

        except Exception:
            pwd = session.pwd()

            session.cwd(file)
            recursive_delete(session)

            session.cwd(pwd)
            session.rmd(file)

        print("Removed: " + file)
```

## Recursive Upload

```python
def recursive_upload(session, directory):
    file_names = [name for name in listdir(directory) if name not in blacklist]

    for file_name in file_names:
        if(isfile(join(directory, file_name))):
            file = open(join(directory, file_name), 'rb')
            session.storbinary('STOR ' + file_name, file)

        else:
            pwd = session.pwd()

            session.mkd(file_name)
            session.cwd(file_name)

            recursive_upload(session, join(directory, file_name))

            session.cwd(pwd)


        print("Uploaded: " + file_name)
```