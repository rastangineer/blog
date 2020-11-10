---
title: "Links 16/11/2020"
date: 2020-11-16T16:20:00
categories:
  - blog
tags:
  - linkdumps
  - learning
---

* [Lost internet access after reboot in my WSL environments](https://github.com/microsoft/WSL/issues/3438#issuecomment-410518578)
  
  This week I received a Windows 10 upgrade which upgraded my WSL to WSL2 also. Everything looked fine until I rebooted my machine, I noticed I lost internet in my WSL Ubuntu's. I found this link and performed the following steps:

```DOS
  netsh winsock reset
  netsh int ip reset all
  netsh winhttp reset proxy
  ipconfig /flushdns
```
  Then reboot Windows.