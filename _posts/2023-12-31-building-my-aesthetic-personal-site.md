---
layout: post
title: "Building My Aesthetic Personal Site 📝"
subtitle: "with a custom Catppuccin Jekyll theme 😺"
author: "HynDuf"
header-style: text
tags:
  - Technical
  - Ricing
---

## Inspiration 
You can now easily change the color to your liking in `less/variables.less` file (at the end there are sections for light and dark mode).

## Preview
Here are some previews of the website.

```c
# f_00_Void_generic_NoX_FR_team_no-kernel.plug
# version="1.2.0"; revision="-rc5"
# Firstrib Void outfitted with a basic command line console,  midnight commander and no kernel
# Creation date 24Sep2021; Revision date: 31Aug2023
# Copyright FR team; License MIT
# 23Aug2023 - Sofiya / 49704

# build this via terminal commands:
# export CONNECTION_TIMEOUT=-1
# ./build_firstrib_rootfs.sh void default amd64 f_00_Void_amd64_noXsimple00_sofiya-120rc5.plug 
# Architecture i386 will probably successfully build too as an alternative to amd64
# passwd -a root / passwd -a spot
# login is user=root passwd=root

# All the parameters/commandlines can be appropriately changed:
# Simply comment in or comment out till you have what you desire
# or add new packages to the xbps-install lists.
# You can add as many valid commandlines as you want in here.
#
# base system
xbps-install -y base-minimal ncurses-base bash eudev
xbps-install -y file mc xterm xauth wmctrl 
xbps-install -y shadow wpa_supplicant  # needed for most wifi
xbps-install -y ntfs-3g zstd 
xbps-install -y xorg rsync

# Create /root directories
#
mkdir -p /root/Desktop
mkdir -p /root/Documents
mkdir -p /root/Downloads
mkdir -p /root/Music
mkdir -p /root/my-applications
mkdir -p /root/Pictures
mkdir -p /root/Public
mkdir -p /root/Startup
mkdir -p /root/Templates
mkdir -p /root/Videos

```
