# Welcome to Lean's  git source of OpenWrt and packages

Note:
--
1. DO **NOT** USE **ROOT** USER TO CONFIGURE!!!

2. Login IP is 192.168.1.1 and login password is "password".

Let's start!
---
First, you need a computer with a linux system. It's better to use Ubuntu 18 LTS 64-bit.

Next you need gcc, binutils, bzip2, flex, python3.5+, perl, make, find, grep, diff, unzip, gawk, getopt, subversion, libz-dev and libc headers installed.

To install these program, please login root users and type
`
sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch python3.5 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib
`
in terminal

Third, logout of root users. And type this `git clone https://github.com/coolsnowwolf/lede` in terminal to clone this source.

After these please type `cd lede` to cd into the source.

Please Run `./scripts/feeds update -a` to get all the latest package definitions
defined in `feeds.conf` / `feeds.conf.default` respectively
and `./scripts/feeds install -a` to install symlinks of all of them into
`package/feeds/` .

Please use `make menuconfig` to choose your preferred
configuration for the toolchain and firmware.

Use `make menuconfig` to configure your image.

Simply running `make` will build your firmware.
It will download all sources, build the cross-compile toolchain,
the kernel and all choosen applications.

To build your own firmware you need to have access to a Linux, BSD or MacOSX system
(case-sensitive filesystem required). Cygwin will not be supported because of
the lack of case sensitiveness in the file system.

Note: Addition Lean's private package source code in `./package/lean` directory. Use it under GPL v3.  
GPLv3 is compatible with more licenses than GPLv2: it allows you to make combinations with code that has specific kinds of additional requirements that are not in GPLv3 itself. Section 7 has more information about this, including the list of additional requirements that are permitted.


本项目基于lean源码修改自用二次发布，更多支持请访问原项目。  
the Original project  https://github.com/coolsnowwolf/lede
