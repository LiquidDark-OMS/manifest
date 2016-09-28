
LiquidDark Source 
----------------------

<img src="https://raw.githubusercontent.com/LiquidDark-OMS/android/mm6.0/LiquidDark-Logo.png">
===================

Thanks 
- liquid0624
and more

Build Environment
--------------------
- Official build environment as per Google and AOSP [Android source page](http://source.android.com/source/index.html)
- XDA user guides [Ubuntu 14.04 Trusty LTS](http://forum.xda-developers.com/showthread.php?t=2639611) , 
[Ubuntu 14.10 Utopic](http://forum.xda-developers.com/chef-central/android/howto-setup-ubuntu-14-10-utopic-unicorn-t2862442) , 
[Arch Linux](https://wiki.archlinux.org/index.php/android#Building_Android)

Initialize Source
--------------------
You will need to set up some directories in your build environment.

To create them run:

    mkdir -p ~/bin
    mkdir -p ~/liquid
    
    Enter the following to download the "repo" binary:

    curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

    chmod a+x ~/bin/repo

You may need to reboot for these changes to take effect. 
Now enter the following to initialize the repository:

    cd ~/liquid

    repo init -u git://github.com/LiquidDark-OMS/manifest.git -b ng

Sync Source
--------------------
    repo sync -jx -f (x being however many cpu jobs, you can also use -c to sync only the current branch specified by repo init)

Build Source
--------------------
   . build/envsetup.sh

Choose Device
--------------------
    lunch nougat_bullhead-userdebug

Clean Builds
--------------------
- cd ~/liquid
- repo sync -jx -f (x being however many cpu jobs, may also use -c as above)
- lunch and pick the right device (refer to above for choosing right device to build)
- make clean
- mka liquid
﻿
