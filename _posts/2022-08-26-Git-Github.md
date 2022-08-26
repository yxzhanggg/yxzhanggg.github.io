---
layout: post
title:  Git and Github quick start
date:   2022-08-26
---

# Configure Github

## Configure local git

```shell
git config --global user.name "user.name"
git config --global user.email "user.email"
```

## Generate ssh file

```sh
ssh-keygen -t rsa
```

Copy everything in `~/.ssh/id_rsa.pub` to SSH setting of your `github repository`

## Test connection

```sh
ssh -T git@github.com
```
