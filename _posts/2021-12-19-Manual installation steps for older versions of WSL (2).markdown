---
layout: post
title:  "Manual installation steps for older versions of WSL (2)"
date:   2021-12-19 20:50:47 +0700
categories: jekyll update
---
## In this article

> Step 4 - Download the Linux kernel update package  
> Step 5 - Set WSL 2 as your default version  
> Step 6 - Install your Linux distribution of choice  
 
For simplicity, we generally recommend using the wsl --install to install Windows Subsystem for Linux, but if you're running an older build of Windows, that may not be supported. We have included the manual installation steps below. If you run into an issue during the install process, check the installation section of the troubleshooting guide.

---

# Step 4 - Download the Linux kernel update package

1. Download the latest package: [WSL2 Linux kernel update package for x64 machines](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

2. Run the update package downloaded in the previous step. (Double-click to run - you will be prompted for elevated permissions, select ‘yes’ to approve this installation.)

Once the installation is complete, move on to the next step - setting WSL 2 as your default version when installing new Linux distributions. (Skip this step if you want your new Linux installs to be set to WSL 1).

> Note
> 
> For more information, read the article changes to updating the WSL2 Linux kernel, available on the Windows Command Line Blog.

---

# Step 5 - Set WSL 2 as your default version

Open PowerShell and run this command to set WSL 2 as the default version when installing a new Linux distribution:

```
wsl --set-default-version 2
```

---

# Step 6 - Install your Linux distribution of choice

1. Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.

![](https://docs.microsoft.com/en-us/windows/wsl/media/store.png)

The following links will open the Microsoft store page for each distribution:

* [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
* [Ubuntu 20.04 LTS](https://www.microsoft.com/store/apps/9n6svws3rx71)
* [openSUSE Leap 15.1](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
* [SUSE Linux Enterprise Server 12 SP5](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
* [SUSE Linux Enterprise Server 15 SP1](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
* [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
* [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
* [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
* [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
* [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
* [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)
* [Raft(Free Trial)](https://www.microsoft.com/store/apps/9msmjqd017x7)

2. From the distribution's page, select "Get".

![](https://docs.microsoft.com/en-us/windows/wsl/media/ubuntustore.png)

The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC. All future launches should take less than a second.

You will then need to [create a user account and password for your new Linux distribution](https://docs.microsoft.com/en-us/windows/wsl/setup/environment#set-up-your-linux-username-and-password).

![](https://docs.microsoft.com/en-us/windows/wsl/media/ubuntuinstall.png)

**CONGRATULATIONS! You've successfully installed and set up a Linux distribution that is completely integrated with your Windows operating system!**

---

**Back** [Manual installation steps for older versions of WSL (1)](http://localhost:4000/jekyll/update/2021/12/18/Manual-installation-steps-for-older-versions-of-WSL-(1).html)

---
Reference  
[Manual installation steps for older versions of WSL](https://docs.microsoft.com/en-us/windows/wsl/install-manual), Windows technical documentation, Dec. ,19,2021

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
