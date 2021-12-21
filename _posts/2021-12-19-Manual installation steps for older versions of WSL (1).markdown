---
layout: post
title:  "Manual installation steps for older versions of WSL (1)"
date:   2021-12-19 20:39:47 +0700
categories: jekyll update
---
## In this article

> Step 1 - Enable the Windows Subsystem for Linux  
> Step 2 - Check requirements for running WSL 2  
> Step 3 - Enable Virtual Machine feature  

For simplicity, we generally recommend using the wsl --install to install Windows Subsystem for Linux, but if you're running an older build of Windows, that may not be supported. We have included the manual installation steps below. If you run into an issue during the install process, check the installation section of the troubleshooting guide.

---

# Step 1 - Enable the Windows Subsystem for Linux

You must first enable the "Windows Subsystem for Linux" optional feature before installing any Linux distributions on Windows.

Open PowerShell as Administrator (Start menu > PowerShell > right-click > Run as Administrator) and enter this command:

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
We recommend now moving on to step #2, updating to WSL 2, but if you wish to only install WSL 1, you can now **restart** your machine and move on to Step 6 - Install your Linux distribution of choice. To update to WSL 2, **wait to restart** your machine and move on to the next step.

---

# Step 2 - Check requirements for running WSL 2

To update to WSL 2, you must be running Windows 10.

* For x64 systems: Version 1903 or higher, with Build 18362 or higher.
* For ARM64 systems: Version 2004 or higher, with Build 19041 or higher.
* Builds lower than 18362 do not support WSL 2. Use the [Windows Update Assistant](https://www.microsoft.com/th-th/software-download/windows10) to update your version of Windows.

To check your version and build number, select **Windows logo key + R**, type winver, select OK. Update to the latest Windows version in the Settings menu.

---

# Step 3 - Enable Virtual Machine feature

Before installing WSL 2, you must enable the **Virtual Machine Platform** optional feature. Your machine will require [virtualization capabilities](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed) to use this feature.

```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
**Restart** your machine to complete the WSL install and update to WSL 2.

---
**Next** [Manual installation steps for older versions of WSL (2)](http://localhost:4000/jekyll/update/2021/12/18/Manual-installation-steps-for-older-versions-of-WSL-(2).html)

---
Reference  
[Manual installation steps for older versions of WSL](https://docs.microsoft.com/en-us/windows/wsl/install-manual), Windows technical documentation, Dec. ,19,2021


[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
