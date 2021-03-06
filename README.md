# supayuzamenyu (for google chromebooks)
Quick and easy menu for installing and launching Ubuntu (using Crouton and Crucial) on chromebooks and boxes

It uses [Crouton](https://github.com/dnschneid/crouton), the Chromium OS universal chroot environment and [crouton-crucial](https://github.com/qrkourier/crouton-crucial), Helper scripts for Crouton

## Advantages
* easy to launch Ubuntu windows or environments
* easy to install Ubuntu windows or environments
* easy to delete Ubuntu environments

## Installing Crouton Extension
* install the [crouton extension from Chrome Store](https://goo.gl/OVQOEt), which provides integration with Chromium OS so that can copy/cut/paste to and from Chrome and Ubuntu.  Also enables Ubuntu windows and tabs in Chrome.

## Installing menu
* enter developer mode (see [developer mode](./developer_mode.md))
* download and unzip [the zip file](https://github.com/ezzye/supayuzamenyu/archive/master.zip)
* press ctrl-alt-t to open a crosh terminal see [10+ Commands Included In Chrome OS’s Hidden Crosh Shell](http://www.howtogeek.com/170648/10-commands-included-in-chrome-oss-hidden-crosh-shell/)
* invoke bash as root
```
crosh> shell
```
* run supayuzamenyu to install menu
```
$ sudo bash ~/Downloads/supayuzamenyu-master/supayuzamenyu.sh
```
* this opens a new Ubuntu enviroment

## Starting menu
* run menu command to start menu in a new shell window then select number to do that menu item
```
$ bash menu
```
* example menu

```
--Launch-- Full Ubuntu (full Ubuntu in separate environment)
--Launch-- Ubuntu (Ubuntu in Chrome window)
--Launch-- Terminal (Ubuntu terminal in Chrome tab)
--Launch-- An Ubuntu Application in a Tab (e.g. gimp)
--Launch-- An Ubuntu Application in a Window (e.g. gimp)
--Quit menu ------------------------------------------------
--Delete-- Delete Ubuntu (deletes all instances of Ubuntu)
--Create-- Create a NEW Ubuntu (this takes a long while then launches in Chrome Window)
Please enter your choice (number):


```
* You can re-enter menu at any time by typing `bash menu` at the shell prompt `$`.

* IMPORTANT when creating a new Ubuntu enviroment last step seems to be entering a user name but you need to return then enter a password (then return) and then re-enter same password (then return) to complete setup.  

## Ununtu target file installation menu

* when you are in Ubuntu you can open up another menu by typing `menu` at prompt:

```
$ menu
1) --Install-- Minecraft Game
2) --Install-- Eclipse Integrated Development Editor
3) --Install-- Gimp Image Editor
4) --Install-- Alacarte Ubuntu Menu builder
5) --Quit menu ------------------------------------------------
Please enter your choice (number):
```
* this contains script to install popular software
* Feel free to make pull requests or issues with new installation scripts for chromebook Ubuntu software
* PLEASE BEAWARE THAT YOU ARE USING THIS SOFTWARE (supayuzameny) SOLELY AT YOU OWN RISK


## Files for advanced users
* optionally, before creating new Ubuntu edit crucial.rc file (~/Downloads/crouton-crucial-master/crucial.rc)
* crucial.rc: annotated runcom file for Crouton environments; required by crucial.sh; edit this first
* crucial.sh: starts a Crouton chroot; optionally first installing, backing up, or updating
* keepawake.sh: a wrapper script optionally called by crucial.sh that disables suspend before enter-chroot
