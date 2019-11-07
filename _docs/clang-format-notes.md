---
title: Clang Format Notes
permalink: /system/clang-format-notes
layout: default
---

# Clang Format Notes

The intention is to activate use the integrated VS2017 clang-format on save. The currently shipped version of clang-format in VS2017 is clang-format 6.0.0.

## Install Format document on Save

1. Install plugin
[Format document on Save](https://marketplace.visualstudio.com/items?itemName=mynkow.FormatdocumentonSave)

2. Example of configuration of plugin
![Config of plugin VS2017]({{site.baseurl}}/assets/images/format-on-save-plugin.png )

3. Enable use of clang-format in VS2017

Make sure "Enable ClangFormat support" is checked 

![Config of clang-format VS2017]({{site.baseurl}}/assets/images/enable-clang-format-vs2017.png)


## Use with PowerShell
If you need to do apply clang format on all files, it is useful to use PowerShell

1. Add clang-format to path. Use the same executable as shipped with VS2017 installation

```
C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\VC\vcpackages\clang-format.exe
```

2. Script to apply clang-format on header/cpp files in a folder recursively
```
dir -recurse -include *.cpp,*.h | %{clang-format -i $_.FullName}
```

## References
https://clang.llvm.org/docs/ClangFormat.html



# Obsolete 

### The following extension will miss some single space formatting in some cases - DO NOT USE

https://marketplace.visualstudio.com/items?itemName=LLVMExtensions.ClangFormat

### NB obsolete!! Use from Windows SubSystem for Linux

These instructions will enable use of clang format 5 recursively on a folder on Windows using WSL(Windows Subsystem for Linux). The file system is by default shared with Windows.

1. Activate Windows Subsystem for Linux, use Ubuntu 16.04, https://docs.microsoft.com/en-us/windows/wsl/install-win10
2. Install clang-format-5.0, based on https://gist.github.com/Ouroboros/0beec448f61c9926023633ca532184dc
```
wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | sudo apt-key add -
sudo apt-add-repository "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-5.0 main"
sudo apt-get update
sudo apt-get install -y clang-format-5.0
```

3. Set working folder to the root folder to recursive apply clang-format. The default behaviour is to search upwards for a .clang-format configuration file.

```
cd /mnt/d/..../...
find  -iname *.h -o -iname *.cpp | xargs clang-format-5.0 -i
```

## References
https://docs.microsoft.com/en-us/windows/wsl/install-win10

https://clang.llvm.org/docs/ClangFormat.html
