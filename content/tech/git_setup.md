---
title: "Setup git in new device"
date: 2026-09-20
---

[Guide](https://git-scm.com/book/ms/v2/Getting-Started-Installing-Git)

Setup git and link to personal github repo in new deivce in Fedora

## Install basic git tools

```bash
sudo dnf install git-all
```

## Install git from source

```bash
sudo dnf install dh-autoreconf curl-devel expat-devel gettext-devel openssl-devel perl-devel zlib-devel
```
In order to be able to add the documentation in various formats (doc, html, info), these additional dependencies are required:

```bash
sudo dnf install asciidoc xmlto docbook2X
sudo dnf install getopt
sudo ln -s /usr/bin/db2x_docbook2texi /usr/bin/docbook2x-texi
```
## First-time git setup

```bash
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

You can view all of your settings and where they are coming from using:

```bash
git config --list --show-origin
```

To set main as the default branch name do:

```bash
git config --global init.defaultBranch main
```
