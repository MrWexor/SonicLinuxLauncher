This is a slightly modified version of the rewritten Sonic 4: Episode I
launcher made by darealshinji, here made to be specifically compiled
on Linux, avoidving the use of Visual Studio and using the Linux version
of MingGW.

The original launcher by Sonic Team was written in Java, but the game itself uses no Java.
This rewrite is made to avoid a pointless Java runtime dependency and to make it easier
to run Sonic 4 on Linux using Wine or Proton.

How to build
------------
This was tested on Arch Linux, but should work fine on any distro. The instructions below are
specific for Arch, so check out which packages should you use on your own distro.

Install MingGW for GCC:
```
sudo pacman -S mingw-w64-gcc
```

Install git if you don't have it on your system:
```
sudo pacman -S git
```

Clone this repo using git:
```
sudo git clone https://github.com/MrWexor/sonic-4-launcher-linux
```

Go to the repo directory created by git in the terminal and checkout the submodules:
```
cd sonic-4-launcher-linux
git submodule init && git submodule update
```

Use make to start compiling:
```
make
```

After compiling, the Windows executable should be in the 'out' directory.

License
-------
Most of the stuff is MIT licensed, check the source file headers for details.
This project is using the FLTK library which is LGPLv2 licensed but with certain exceptions,
see fltk/COPYING for details. The image files are copyrighted and not under a free license.
