Natron on Windows
==================

Scripts used to build and distribute [Natron](http://www.natron.fr) on Windows.

Build server installation
=========================

Any Unix machine with GCC >= 4 and git installed.
These scripts make use of [MXE](http://mxe.cc) to operate.  

Install MXE where you want:
    
    cd ~/development
    git clone https://github.com/mxe/mxe.git

Now clone this repository 

    cd ..
    git clone https://github.com/MrKepzie/natron-mingw-cross
    cd natron-mingw-cross


Create the local.sh file in the root of natron-mingw-cross to specify various infos, e.g:

    #!/bin/sh

    MXE_INSTALL=/Users/<username>/development/mxe
    REPO_DEST=mrkepzie@vps163799.ovh.net:../www/downloads.natron.fr
    REPO_URL=http://downloads.natron.fr
    

If MXE_INSTALL is not specified then it will use the MXE submodule

RHEL/CentOS 7.x requirements:

```
yum install -y epel-release
yum install wget git autoconf automake bash bison bzip2 cmake flex gcc-c++ gettext git gperf intltool make sed libffi-devel libtool openssl-devel p7* patch perl pkgconfig python ruby scons unzip wget xz glibc-devel.i686 libstdc*.i686
```
