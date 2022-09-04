---
title: /UNIX
layout: page
permalink: /UNIX/
---
# I/O
buffered I/O: store the data in blocks of buffers, then read/write.

unbuffered I/O: read/write data char by char (atom operation). [invokes a system call in kernel]

File descriptor
- standard input: 0
- standard output: 1
- standard error : 2
```sh
# The I/O is directed to 3 file descriptors by default
# Redirection: replace the file descriptors by certain file
prog < infile > outfile
# Pipe: the command still have defualt I/O, and pipe connects the I/O between files
prog1 | prog2 | prog3
