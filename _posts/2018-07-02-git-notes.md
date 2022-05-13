---
layout: post
title: Git and GitHub
categories: notes
last_modified_at: 2020-07-14 11:19:55
---

Git is version control software to track changes in source code. GitHub is cloud storage for Gits.

- Do not remove this line (it will not be displayed)
{:toc}

## What is Git

- Git is a distributed version-control system (VCS) for tracking changes in source code during software development.
- We check-in and check-out files to git and it keeps a track of the history.
- On mac it was pre installed as part of Xcode Command Line Tools.
- `git --version` to check the version of git installed.

## How to clone a repository from GitHub.com

- `git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY`
- eg, `git clone https://github.com/miguelgrinberg/microblog.git`
- This will bring all the files from remote to local directory with git repository on local folder.
- Now if you have permission to commit to this repo then you can **authenticate to push**, else **change the remote** to another repo that you can push to.

## How to set up Git on a Local Folder

Setup Git

- On any folder, do this **once**
- eg, `mkdir myProject` then `cd myProject`
- `git init` this will create a **local** git repository on your local drive. Now if you need to add this to a remote git repository, for example, a repository on github.com or bitbucket then you need to add remote to this folder.

Now once you have written your code, you can add and commit new code to local git:

Add and Commit code

- `git add .` adds all files to git. To add one file, pass filename.
- `git diff` shows changes made to files.
- `git commit -m "Message"` commits to git with message.
- optional, `cat .gitignore` add files that you want git to ignore

Add Remote

- Create a new repository on GitHub.com
- on your local folder, `git remote add  [name] [url]` will add remote. Here, `name` can be origin and `url` is https/ssh url of git repo created online on GitHub.com. Use SSH if you have SSH authentication setup.
- Once remote is added to your local git then you can push or pull the files based on the commands below.

Syncing local and remote

- `git pull` pulls updates from remote to local
- `git push` pushes the committed changes from local to remote. We can also specify remote name and branch here. eg:
  - `git push -u origin master`.

## SSH Authentication to push to remote

You can connect to GitHub using the Secure Shell Protocol (SSH), which provides a secure channel over an unsecured network. It can help connect one machine to another using keys and thus avoiding to provide username and password/token on each request. `id_rsa.pub` is default public key.

- if `~/.ssh/id_rsa.pub` exists do `cat ~/.ssh/id_rsa.pub` else generate SSH Key `ssh-keygen`, passphrase is optional.
- copy the content, Open GitHub, click your profile icon, settings, SSH and GPC Keys, Click on the new ssh key button.
- enter any title and key that you copied
- more - <https://docs.github.com/en/authentication/connecting-to-github-with-ssh>

Checking

- Check using `ssh -T git@github.com`
- Output should say `Hi <user_name>! You've successfully authenticated, but GitHub does not provide shell access.`

Fixing SSH issue

- error - `ssh: connect to host github.com port 22: Connection refused`
- change ssh config to use new url and port, Override SSH settings `gedit ~/.ssh/config` and add

```sh
# Add section below to it
Host github.com
  Hostname ssh.github.com
  Port 443
```

- save and try again.
- Change your git remote to use SSH URL instead of HTTPS `git remote set-url origin git@github.com:YOUR-USERNAME/REPO-NAME.git`

## Get and Set Remotes

- `git remote -v` do on a folder to check remotes added.
- `git remote get-url --all REMOTE-NAME` to see URL of remote.
- `git remote set-url origin https://github.com/YOUR-USERNAME/YOUR-REPO.git` to update remote on a folder.

## Handling Conflicts

If you push to git from two different repositories then there may be conflict. eg, you push from mac repo and a cloud repo or ubuntu repo. To handle conflict:

- Open conflicted file in editor and look for `<<<<<<<<` .
- You'll see the changes from the HEAD or base branch (github usually) after the line `<<<<<<< HEAD`
- `========`, it divides your changes from the other branch as `>>>>>>>>YOUR_BRANCH_NAME`
- You can decide if you want keep your branch changes or not. If you want to keep the changes what you did, delete the conflict marker they are, `<<<<<<<, =======, >>>>>>>` and then do a merge.
- Once done, `add commit push` :)

## Version controlling in GIT

You can see previous versions of file in your git repository.

- to see the checkins done

```sh
> git reflog
044cf0e (HEAD -> master) HEAD@{0}: commit: updates
aae1995 HEAD@{1}: commit (initial): first commit
```

- `git show HEAD@{1}:path/to/file.ext` show file on terminal
- press down arrow to navigate and `q` to quit

or

- `git show -1 filename` - shows difference with last revision
- use -1 or -2 or -3 and so on for going into history.

## Adding RSA for password free sync on Mac

GitHub is excellent for code repositories online to share work, collaborate or keep a backup.

I have followed an excellent [post](https://kbroman.org/github_tutorial/) by Karl Broman on the same. To summaries the flow:

- Install git on local drive.
- Setup RSA for SSL: RSA is used for making safe authentications via SSL.
- Setup GitHub Account: You will get an online space to upload your code with version controlling.

**Related Posts**:

- Further to this post, [Set up Github Pages and Jekyll](github-pages-jekyll) to get started with blogging and personal site.
