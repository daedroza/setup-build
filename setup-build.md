
Setting up your build environment for Ubuntu/Mint
=================================================

Prepare your Java environment
-----------------------------
In terminal:
------------
```
sudo apt-get purge openjdk-\* icedtea-\* icedtea6-\*
sudo apt-get update
sudo apt-get install openjdk-8-jdk
```
Install some required tools:
----------------------------
```
sudo apt-get install liblz4-tool git-core gnupg ccache lzop flex bison gperf build-essential zip curl zlib1g-dev zlib1g-dev:i386 libc6-dev lib32ncurses5 lib32z1 lib32ncurses5-dev x11proto-core-dev libx11-dev:i386 libreadline6-dev:i386 lib32z-dev libgl1-mesa-glx:i386 libgl1-mesa-dev g++-multilib tofrodos python-markdown libxml2-utils xsltproc readline-common libreadline6-dev libreadline6 libncurses5-dev lib32readline6 libreadline-dev libreadline6-dev:i386 libreadline6:i386 bzip2 libbz2-dev libbz2-1.0 libghc-bzlib-dev libsdl1.2-dev libesd0-dev squashfs-tools pngcrush schedtool python maven liblz4-tool
```
If you come into any errors:
----------------------------
```
sudo apt-get update && sudo apt-get upgrade
```
Then try again

Download repo tool and set your path
------------------------------------
```
mkdir ~/bin
curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
chmod a+x ~/bin/repo
```
Include bashrc in repo tool
---------------------------
```
sudo nano ~/.bashrc
```
Once open: To set the right path for your local bin folder, paste the following code to a new line at the very bottom of the bashrc file, and then save the file using Ctrl+X

Add:
```
export PATH=~/bin:$PATH
export USE_CCACHE=1
```
After saving and closing:
```
source ~/.bashrc (Reload bash variables to include the new path)
```
Install lz4 compression tool:
-----------------------------
```
sudo apt-get install liblz4-tool

Setting up global:
------------------
```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```
(Just replace the credentials with your own)

When that is done & repo is synced, type:
-----------------------------------------
```
Set ccache : prebuilts/misc/linux-x86/ccache/ccache -M 50G
```

Have Fun!!
----------
