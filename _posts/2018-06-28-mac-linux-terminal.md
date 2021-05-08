---
layout: post
title: Mac and Linux Ways
categories: notes snippets
last_modified_at: 2021-05-06 13:57:56
---

Here are some basic understandings and commands that can be used on UNIX terminal and eventually on Mac. 


## Mac Specific


### Homebrew
- package manager for mac, 
  - cask are usually GUIs apps like Sublime
  - formulae are packages, CLIs, like node

Brew Global Commands:
- `brew update` - Update brew and cask list, not packages
- `brew upgrade` -  Upgrade all packages
- `brew list` - List installed packages and casks
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
- `brew install --cask firefox` Install the Firefox browser
- `brew list --cask`  List installed applications

### Others

`diskutil list` - lists all disks

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

Ubuntu is debain based os, others are Mint, Elementary and PoP OS.

Debain uses dpkg packaging system, for install/uninstall software.

Packages are maintained in **repositories**, Main, Universe, Restricted and Multiverse. 

`sudo add-apt-repository universe` to enable a repo.

PPA - Personal Package Archive - allows application developers to create their own repositories to distribute.

`sudo add-apt-repository ppa:mkusb/ppa` add a ppa repo

**APT - Advanced Package Tool** is CLT UI that works with core libraries to handle the installation and removal of software on Debian, Ubuntu. IT manages dependencies, config files and upgrades/downgrades.

`apt-get` performs installation, search, updates to pkg available on system. works with `sudo` only.

`sudo apt-get update` - updates local copy of packages database. The result has :
- Hit: no change in pkg
- Get: update available, downloads details but not the update
- Ign: ignores.

`sudo apt-get upgrade` updates core system and apps installed. For one package update `sudo apt-get upgrade [package_name]`.

`sudo apt-get install [pkg1] [pkg2]` if you know the name of apps.

`sudo apt-get remove [package_name]` to uninstall. but kepps config files.

`sudo apt-get autoremove` cleans up unwanted pkg.

`apt list --installed` see all that's installed.

apt=most common used command options from apt-get and apt-cache. It is high level wrapper on old apt-get. Use apt for better UI and info like summary and progress bar.

Install a `.deb` file, eg, Chrome:
- `sudo dpkg -i /path/to/foo.deb` installs. 
- `sudo apt-get install -f` fix-broken dependencies.

Or simply use below to install with dependecies
- `sudo apt install ./name.deb`

`dpkg` does not handle dependency, while `apt` does. apt under the hood uses dpkg.

Virtual box add on:
- `sudo apt update`
- `sudo apt install virtualbox-guest-dkms virtualbox-guest-x11 virtualbox-guest-utils`

Install nsepa and Citrix Workspace:

- `wget http://ftp.br.debian.org/debian/pool/main/n/network-manager/libnm-util2_1.6.2-3+deb9u2_amd64.deb http://ftp.br.debian.org/debian/pool/main/n/network-manager/libnm-glib4_1.6.2-3+deb9u2_amd64.deb` download debs
- `sudo apt install ./libnm-util2_1.6.2-3+deb9u2_amd64.deb ./libnm-glib4_1.6.2-3+deb9u2_amd64.deb` install the debs downloaded

- Download .deb file from Citrix, amd 64
- `cd ~/Downloads`
- `sudo dpkg -i icaclient_21.4.0.11_amd64.deb`
- `sudo apt-get install -f`

Install Jupyter notebook:
- `sudo apt-get update`
- `sudo apt install python3-pip` PIP is required for Jupyter
- `sudo -H pip3 install --upgrade pip` upgrade pip, -h for sudo to take home dir of root rather than current user. Prevents user dir to be owned by root.
- `sudo -H pip3 install virtualenv` to create virtual envs
- `mkdir jupyter && cd jupyter`
- `virtualenv env` create env named env
- `source env/bin/activate` activate it
- `pip install jupyter` install jupyter
- `jupyter notebook` run it


### Others

`lsblk` lists disk

### Users and Groups

List all users 
- `getent passwd`
- `compgen -u`
- `cut -d: -f1 /etc/passwd`

List all groups
- `compgen -g`

Add user to group - `sudo adduser username group`

### OS Setup and Virtualization

USB Installation
- works like a charm, 
- make a bootable live usb/cd - https://linuxhint.com/create_bootable_linux_usb_flash_drive/
- boot from it and install to another USB - https://www.fosslinux.com/10212/how-to-install-a-complete-ubuntu-on-a-usb-flash-drive.htm
- space and drive speed is a issue.
- Clean grub of mac - https://apple.stackexchange.com/questions/337189/unwanted-grub-on-macos-high-sierra
- Tripe boot mac - https://www.youtube.com/watch?v=B0EuYHFeLAA
- First steps on Ubuntu - https://www.youtube.com/watch?v=GrI5c9PXS5k

## Linux Ways

ENVs:
- `source activate [path to env]` activates env
- `source deactivate ` deactivates enn

Emac Basic
- Press `ctrl + c + x` to save and exit a file.

Other
- everything global is installed in `/usr/local/bin/`
- use PostMan for http requests to REST routes

- `rmdir` removed empty dir
- `rm -rf` removes non/empty dir and files forcefully
- `rm` removes files not directories.





