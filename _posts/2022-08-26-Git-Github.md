---
layout: post
title:  Git and Github quick start
date:   2022-08-26
---

# Configure Github

1-Configure local git

```sh
git config --global user.name "user.name"
git config --global user.email "user.email"
```

2-Generate ssh file

```sh
ssh-keygen -t rsa
```

Copy everything in `~/.ssh/id_rsa.pub` to SSH setting of your `github repository`

3-Test connection

```sh
ssh -T git@github.com
```
