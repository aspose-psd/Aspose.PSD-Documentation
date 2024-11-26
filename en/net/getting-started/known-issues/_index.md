---
title: Known Issues
type: docs
weight: 40
url: /net/known-issues/
---

## **.NET Compact Framework**
- It is observed that on some specific windows versions such as Windows Mobile 5.0-6.0 the compact framework assemblies signed with certificate (or dual signed certificates) does not work as expected and are not able to load correctly (a TypeLoadException is thrown). To overcome the issue the user needs to remove any certificate and then use the updated assembly. Please note that you make this on your own risk and we do not guarantee valid work due to such assembly change. Nor we ship assemblies without signature since this is a potential security threat. Instead customers should avoid using such old operating systems, if possible, and/or upgrade the operating system to newer editions or service packs which resolve certificate signing issue.
