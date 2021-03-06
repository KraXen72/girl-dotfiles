# Overview

My current bspwm setup is as shown:

![.](scrots/desktop-1-scrot.png)

<details>
<summary>Repo Navigation</summary>

- [Installation](https://github.com/co1ncidence/dotfiles#installation)
- [Polybar Configuration](https://github.com/co1ncidence/dotfiles#polybar-configuration)
- [Rofi Menus](https://github.com/co1ncidence/dotfiles#rofi-menus)
- [Custom Firefox Build](https://github.com/co1ncidence/dotfiles#custom-firefox-build)

</details>

## Installation

### Dependencies

#### Fonts required:

+ **CozetteVector** [here](https://awesomeopensource.com/project/slavfox/Cozette)
+ **Font Awesome 5 Free Desktop** [here](https://fontawesome.com/download)
+ **Material Icons** [here](https://github.com/google/material-design-icons/tree/master/iconfont)
+ **Hurmit Nerd Font Mono** [here](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Hermit)
+ **Comfortaa** [here](https://www.deviantart.com/aajohan/art/Comfortaa-font-105395949)

#### Programs required (and of course their dependencies as well):

+ **Polybar**: because common sense
+ **Ncmpcpp**: as a music player (cmus is an alternative is mpd is finnicky for you)
+ **Bspwm**: window manager
+ **Cava**: audio visualizer 
+ **Firefox Nightly (latest build)**: if you want to use my custom firefox build
+ **Rofi**: for app launching and various operation menus (for more see [here](https://github.com/co1ncidence/dotfiles#rofi-menus))
+ **All of the dependencies mentioned** [here](https://github.com/adi1090x/rofi#dependencies)


### Installing all configs

clone (or download as ZIP) this repository

```bash
git clone https://github.com/co1ncidence/dotfiles.git
```

from here you can chose which of my configs you want to use and replace your config files with mine (making sure that you back them up first as well), for the configs that require more in-depth installation procedures, I have tutorials below so see if what you want is down there. And my apologies if it isn't since this repo is still a WIP (as of now)

## Polybar Configuration

### Installing my Polybar config

first, back up your current polybar config:
```bash
cd ~/.config/polybar && cp config config-backup
```
now finally
```bash
rm config && rm launch.sh
```
then, cd to my polybar config
first, cd to this directory (this will only work if you cloned my repo into your `/home` directory:
```bash
cd dotfiles/config/polybar
```
next, copy the launch.sh file into your polybar config folder:
```bash
cp launch.sh ~/.config/polybar/
```
and do the same with the actual config file
```bash
cp config ~/.config/polybar/
```
finally, lets see if the bar will launch properly (this will only work if you have polybar, its dependencies and all required fonts installed on to your system):
```bash
cd ~/.config/polybar && launch.sh
```
if all goes well, your bar should end up looking something like this:

![.](scrots/scrot-polybar.png)

#### Here are some (3 lulw) cool features of my polybar:

+ left-clicking the power button on the top left will open up my powermenu (more on that down below)
+ scrolling down and up on the volume logo will increase and decrease the volume respectively
+ the tray is separate from other modules so it doesnt take up unnecessary space or become annoying after 3 entries

## Rofi menus

Here are the rofi menus I use, all credit goes to [adi1090x](https://github.com/adi1090x/rofi) for his amazing work creating these

|Powermenu|Apps|Network|Scrot|
|--|--|--|--|
|![.](scrots/scrot-powermenu.png)|![.](scrots/scrot-apps.png)|![.](scrots/scrot-network.png)|![.](scrots/scrot-scrot.png)|

|Quicklinks|Brightness|MPD|Frequent Apps|
|--|--|--|--|
|![img](scrots/scrot-quicklinks.png)|![img](scrots/scrot-brightness.png)|![img](scrots/scrot-mpd.png)|![img](scrots/scrot-frequentapps.png)|

The brightness menu is a bit finnicky since I am using Xrandr to change my brightness (instead of the default xbacklight) and as of yet I dont know a way to display current brightness but the brightness up and down functions do work

## Custom Firefox Build

**Most credit for this setup goes to [Akshat46](https://github.com/akshat46) and his [Firefox Config](https://github.com/akshat46/FlyingFox)**, anyhoo, I made this Firefox "build" using the extensions [HNTP](https://addons.mozilla.org/en-US/firefox/addon/humble-new-tab/), [Tree Style Tab](https://addons.mozilla.org/en-US/firefox/addon/tree-style-tab/), and a [Firefox Color](https://addons.mozilla.org/en-US/firefox/addon/firefox-color/) theme

![,](scrots/firefox-scrot.png)

## Installation

### UserChrome.css

My UserChrome.css file can be found in the repo, simply place in the `/chrome` directory in your Firefox profile directory (found by going to about:support)

### Humble New Tab Page Setup

After installing the extension, click the options icon, go to the import/export section, and copy the contents of `firefox/hntp/hntp.css` into the import area, further configuration (i.e. fonts and such) can be done manually through the settings GUI

### Tree Style Tab Setup

After installing the extension, press ctrl + shift + a to go to the extensions management page, select Tree Style Tabs -> Preferences, then scroll down all the way, select "Import" and choose the `firefox/tree-style-tab/treestyletab-config.json` file

### Firefox Color Setup 

My Firefox theme can be found [here](https://addons.mozilla.org/en-US/firefox/addon/find-my-way/), if the link doesn't seem to be working come back in a few hours since it might be still undergoing the code review process



