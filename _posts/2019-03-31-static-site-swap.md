---
layout: post
title: static-site-swap.py
description: A python script built to handle the transfer of this website with ftplib.
categories: [scripts, programming, python]
updated: 2019-05-9
status: finished
links: [source, "https://github.com/stephencz/scripts/blob/master/python/static-site-swap.py"]
custom: []
---

##  static-site-swap.py
The major benefit of a server-side content management system such as WordPress is that content is managed and created on the web server.
Static websites, such as this website, need to have their new content and changes manually uploaded to the server.
While doing this isn't difficult, it does get annoying after a while.

I wrote [static-site-swap.py](https://github.com/stephencz/scripts/blob/master/python/static-site-swap.py) to automate the transfer process of my website.
The script is responsible for both deleting old files and uploading new files.
It does this using Python's FTP module [ftplib](https://docs.python.org/3/library/ftplib.html).

The script has a few variables which can be changed:

```python
host = "" 
username = "" 
password = "" 

whitelist = [".", "..", ".htaccess", ".well-known"] 
blacklist = [] 

server_directory = "" 
local_directory = ""
```

The **host**, **username**, and **password** variables all have to do with connecting to the server. 
The host is the IP address, the username is the FTP account name/login, and the password is the FTP account's password.

**Whitelist** and **blacklist** are lists containing the names of files and directories that either not be uploaded or deleted from the web server.
Whitelist contains the files that will not be deleted, and blacklist contains the files that will not be uploaded.

The **server_directory** variable is the directory on the server which files will be deleted from.
The script navigates to this directory immediately after establishing a connection to the server.
It is important to set this to the correct directory, or you risk deleting important files.
Finally, **local_directory** is the directory on your local machine that you want to upload.

Because FTP doesn't support recursive file deletion or creation out of the box, I had to implement that on my own. 
The recursive deletion function is the most interesting piece of code in the script:

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

A similar function, adapted to recursively upload a folder, is the recursive upload function:

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

