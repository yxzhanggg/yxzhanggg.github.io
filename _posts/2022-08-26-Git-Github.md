---
layout: post
title:  Git and Github quick start
date:   2022-08-26
---

# Configure Github

## configure local git

```shell
git config --global user.name "user.name"
git config --global user.email "user.email"
```

## generate ssh file

```sh
ssh-keygen -t rsa
```

copy everything in `~/.ssh/id_rsa.pub` to SSH setting of your `github repository`

## test connection

```sh
ssh -T git@github.com
```
