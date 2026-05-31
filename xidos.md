---
title: XiDOS
parent: Projects
nav_order: 1
permalink: /xidos
---

# XiDOS

XiDOS is a POSIX compatibility layer for MS-DOS and FreeDOS. Like Cygwin on Windows,
it provides a runtime library and headers that map POSIX APIs onto the host operating
system: chiefly the DOS `INT 21h` interface and the underlying BIOS.

The aim is to let Unix-style software compile and run on real or emulated DOS machines
with minimal changes, including file operations, path translation, process spawning and
a growing slice of the C library.

**Status:** early scaffolding.

[Source on GitHub](https://github.com/Arawn-Davies/XiDOS)

> Page coming together — more technical write-ups soon.
