# Minigalaxy

A simple GOG client for Linux that lets you download and play your GOG Linux games

![screenshot](screenshot.png?raw=true)

## Features

The most important features of Minigalaxy:

- Log in with your GOG account
- Download the Linux games you own on GOG
- Launch them

In addition to that, Minigalaxy also allows you to:

- Select in which language you'd prefer to download your games
- Change where games are installed
- Search your GOG Linux library
- Show all games or just the ones you've installed
- View the error message if a game fails to launch

## System requirements

Minigalaxy should work on the following distributions:

- Debian Buster (10.0) or newer
- Ubuntu 18.10 or newer
- Arch Linux
- Manjaro
- Fedora 31
- openSUSE

Other Linux distributions may work as well. Minigalaxy requires the following dependencies:

- GTK+
- Python 3
- PyGObject 3.30+
- Webkit2gtk with API version 4.0 support
- Python Requests


## Installation

**Ubuntu/Debian**

Download the latest deb package from the [releases page](https://github.com/sharkwouter/minigalaxy/releases) and install it.

**Arch/Manjaro**

Build the [AUR package](https://aur.archlinux.org/packages/minigalaxy). For this you can use an AUR helper, or use the following set of commands:

```shell script
git clone https://aur.archlinux.org/minigalaxy.git
cd minigalaxy
makepkg -si
```

**Fedora**

Available in [Copr](https://copr.fedorainfracloud.org/coprs/atim/minigalaxy/)

```
sudo dnf copr enable atim/minigalaxy -y && sudo dnf install minigalaxy

**openSUSE**

Minigalaxy can be found in the [OBS](https://build.opensuse.org/package/show/games:tools/minigalaxy).
```
zypper ar -f obs://games:tools gamestools
zypper ref
zypper in minigalaxy
```

**Other distributions**

***Without VENV***
```shell script
git clone https://github.com/sharkwouter/minigalaxy.git
cd minigalaxy
bin/minigalaxy
```

***With VENV***
```shell script
git clone https://github.com/sharkwouter/minigalaxy.git
cd minigalaxy
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
bin/minigalaxy
```

## Known issues

Expect to see the following issues:

* Using Minigalaxy without an internet connection does not work
* Changing the installation directory makes Minigalaxy unable to detect previously installed games
* Installed games cannot be removed from within the client yet
* Updating games has not been implemented yet
