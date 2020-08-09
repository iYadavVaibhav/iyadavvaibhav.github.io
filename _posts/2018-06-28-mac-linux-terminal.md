---
layout: post
title: Mac and Linux Ways
categories: notes snippets
last_modified_at: 2020-08-02 12:20:40
---

Here are some basic understandings and commands that can be used on UNIX terminal and eventually on Mac. 

## Linux Ways

Emac Basic
- Press `ctrl + c + x` to save and exit a file.

Other
- everything global is installed in `/usr/local/bin/`
- use PostMan for http requests to REST routes

## Mac Specific


### Homebrew
- package manager for mac, 
  - cask are usually GUI apps like Sublime
  - formulae are packages, CLI,like node

Brew Global Commands:
- `brew update` - Update brew and cask, not packages
- `brew upgrade` -  Upgrade all packages
- `brew list` - List installed packages
- `brew cask list` - List installed Casks
- `brew outdated` - List outdated packages?
- `brew doctor` - Diagnose brew issues
- `brew cleanup` - cleans all packages
- `brew services list`- lists all services installed

Brew Commands:
- `brew install git` -  Install a package
- `brew uninstall git` -  Remove/Uninstall a package
- `brew upgrade git` -  Upgrade a package
- `brew switch git 2.5.0` -  Change versions
- `brew list --versions git`  See what versions you have
- `brew cleanup git` Remove old versions

Brew Cask (GUI) commands:
- `brew cask install firefox` Install the Firefox browser
- `brew cask list`  List installed applications

### Others

Copy to clipboard
- `$ pbcopy < my_filename.ext` it copies the content of file to clipboard.
- It is helpful to quickly copy RSA key to clipboard which you need to paste on, may be, GitHub.

Androids
- `~/.android` - google utility folder
- `avdmanager list avd` - lists all android virtual devices installed.

Uninstalling:
Usually check for following dirs and remove:
- `sudo rm /usr/local/mypkg`
- `sudo rm -rf /usr/local/var/mypkg`
- `sudo rm -rf /usr/local/mypkg*`
- `sudo rm -rf /Library/StartupItems/mypkg*`
- `sudo rm -rf /Library/PreferencePanes/MyPkg*`
- `rm -rf ~/Library/PreferencePanes/MyPkg*`
- `sudo rm -rf /Library/Receipts/mypkg*`
- `sudo rm -rf /Library/Receipts/MyPkg*`

## Ubuntu Specific

List all users 
- `getent passwd`
- `compgen -u`
- `cut -d: -f1 /etc/passwd`

List all groups
- `compgen -g`

Add user to group - `sudo adduser username group`













