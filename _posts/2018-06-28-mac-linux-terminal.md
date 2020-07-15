---
layout: post
title: Mac and Linux Ways
categories: notes snippets
last_modified_at: 2020-07-14 11:19:55
---

Here are some basic understandings and commands that can be used on UNIX terminal and eventually on Mac. 

## Linux Ways

Emac Basic
- Press `ctrl + c + x` to save and exit a file.

Other
- everything global is installed in `/usr/local/bin/`
- use PostMan for http requests to REST routes

## Mac Specific

Copy to clipboard
- `$ pbcopy < my_filename.ext` it copies the content of file to clipboard.
- It is helpful to quickly copy RSA key to clipboard which you need to paste on, may be, GitHub.

## Ubuntu Specific

List all users 
- `getent passwd`
- `compgen -u`
- `cut -d: -f1 /etc/passwd`

List all groups
- `compgen -g`

Add user to group - `sudo adduser username group`