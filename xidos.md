---
title: XiDOS
parent: Projects
nav_order: 1
permalink: /xidos
---

# XiDOS

XiDOS is an experimental POSIX compatibility layer for MS-DOS and FreeDOS. Inspired
by projects such as Cygwin, it provides a runtime library and headers that map POSIX
APIs onto the host operating system: chiefly the DOS `INT 21h` interface and the
underlying BIOS.

The aim is to explore how Unix-style software could compile and run on real or emulated
DOS machines with minimal changes. Work is currently focused on file operations, path
translation, process spawning and parts of the C library.

**Status:** early scaffolding.

[Source on GitHub](https://github.com/Arawn-Davies/XiDOS)

> Page coming together — more technical write-ups soon.
