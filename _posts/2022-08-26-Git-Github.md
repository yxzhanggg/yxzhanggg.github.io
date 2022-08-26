---
layout: post
title:  Git and Github quick start
date:   2022-08-26
---

# Configure Github

1. configure local git

```shell
git config --global user.name "user.name"
git config --global user.email "user.email"
```

2. generate ssh file

```sh
ssh-keygen -t rsa
```

3. copy everything in `~/.ssh/id_rsa.pub` to SSH setting of your `github repository`

4. test connection

```sh
ssh -T git@github.com
```
