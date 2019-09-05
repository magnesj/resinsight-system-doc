---
title: Clang Format Notes
permalink: /system/clang-format-notes
layout: default
---

# Clang Format Notes

These instructions will enable use of clang format 5 recursively on a folder on Windows using WSL(Windows Subsystem for Linux). The file system is by default shared with Windows.

1. Activate Windows Subsystem for Linux, use Ubuntu 16.04, https://docs.microsoft.com/en-us/windows/wsl/install-win10
2. Install clang-format-5.0, based on https://gist.github.com/Ouroboros/0beec448f61c9926023633ca532184dc
```
wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | sudo apt-key add -
sudo apt-add-repository "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-5.0 main"
sudo apt-get update
sudo apt-get install -y clang-format-5.0
```

3. Set working folder to the root folder for a recursive apply of clang format and execute
```
cd /mnt/d/..../...
find  -iname *.h -o -iname *.cpp | xargs clang-format-5.0 -i
```
