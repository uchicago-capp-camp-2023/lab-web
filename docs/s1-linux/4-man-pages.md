---
layout: default
title: Man Pages
nav_order: 5
parent: Introduction to Linux
---

# Man Pages

A man page (short for manual page) documents or describes topics applicable to Linux programming. These topics include Linux programs, certain programming functions, standards, and conventions, and abstract concepts.

To get the man page for a Linux command, you can type:

```
man <command name>
```

For example:

```bash
man ls
```

This command displays a man page that gives information on the `ls` command, including a description, flags, instructions on use, and other information.

Each man page has a description. The `-k` flag for man allows you to search these descriptions using a keyword. For example:

```bash
man -k printf
```

This searches all the descriptions for the keyword `printf` and prints the names of the man pages with matches.

Learning how to ready man pages is an important skill.

## Exercises

By default, the `ls` command does not include files with names that shart with a dot (`.`). The `lab1` directory contains a file that starts with a dot. Use `man` to identify the flag to use with `ls` to include this file when listing the contents of `lab1`.

{:style="text-align:center"}
[Previous](./3-file-system.html){: .btn } [Next](./5-python.html){: .btn }
