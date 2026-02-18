# sddm-eva
[![Ko-fi](https://img.shields.io/badge/support_me_on_ko--fi-F16061?style=for-the-badge&logo=kofi&logoColor=f5f5f5)](https://ko-fi.com/keyitdev)

[sddm-eva](https://github.com/the-og-ago/sddm-eva) is a evangelion themed fork of the [sddm-astronaut-theme](https://github.com/Keyitdev/sddm-astronaut-theme) series of themes for the [SDDM](https://github.com/sddm/sddm/) display manager made by **[Keyitdev](https://github.com/Keyitdev)**.

It's written using the latest version of Qt, which is **Qt6**. Its key features include **virtual keyboard support** and an **installation script**. This theme also support **animated wallpapers**. You can easily change its appearance by modifying just one file.

The theme was created for 1080p. However, they should work well in other resolutions.

## Installation

### Script

download and run the setup.sh to install

### Manual

1. Install **dependencies**

[`sddm >= 0.21.0`](https://github.com/sddm/sddm), [`qt6 >= 6.8`](https://doc.qt.io/qt-6/index.html), [`qt6-svg >= 6.8`](https://doc.qt.io/qt-6/qtsvg-index.html), [`qt6-virtualkeyboard >= 6.8`](https://doc.qt.io/qt-6/qtvirtualkeyboard-index.html), [`qt6-multimedia >= 6.8`](https://doc.qt.io/qt-6/qtmultimedia-index.html)

You may also want to install additional video codecs like h.264.

```sh
sddm qt6-svg qt6-virtualkeyboard qt6-multimedia-ffmpeg     # Arch
sddm qt6-svg qt6-virtualkeyboard qt6-multimedia            # Void
sddm qt6-qtsvg qt6-qtvirtualkeyboard qt6-qtmultimedia      # Fedora
sddm-qt6 libQt6Svg6 qt6-virtualkeyboard qt6-virtualkeyboard-imports qt6-multimedia qt6-multimedia-imports        # OpenSUSE
sddm libqt6svg6 qt6-virtualkeyboard-plugin libqt6multimedia6 qml6-module-qtquick-controls qml6-module-qtquick-effects libxcb-cursor0 # Debian Unstable
```

2. Clone this repository
```sh
sudo git clone --depth 1 https://github.com/the-og-ago/sddm-eva /usr/share/sddm/themes/sddm-eva
```
3. Copy fonts to `/usr/share/fonts/`
```sh
sudo cp -r /usr/share/sddm/themes/sddm-eva/Fonts/* /usr/share/fonts/
```
4. Edit `/etc/sddm.conf`
```sh
echo "[Theme]
Current=sddm-eva" | sudo tee /etc/sddm.conf
```
5. Edit `/etc/sddm.conf.d/virtualkbd.conf`
```sh
echo "[General]
InputMethod=qtvirtualkeyboard" | sudo tee /etc/sddm.conf.d/virtualkbd.conf
```

## Selecting a theme

You can select theme by editing [metadata](./metadata.desktop) (`/usr/share/sddm/themes/sddm-eva/metadata.desktop`).

Just edit this line:
```
ConfigFile=Themes/eva.conf
```
All available configs are in [Themes](./Themes/) directory.

## Previewing a theme

You can preview the set theme without logging out by runnning:
```sh
sddm-greeter-qt6 --test-mode --theme /usr/share/sddm/themes/sddm-eva/
```
> Note that depending on the system configuration, the preview may differ slightly from the actual login screen.

## Sources

Initially the theme was independed fork of [MarianArlt's theme](https://github.com/MarianArlt/sddm-sugar-dark) but now the project has come a long way and started to significantly deviate from the original.
Many of the wallpapers and fonts used in this project are very popular and copied from one user to another, so I don't know who the original creator is. 
I also redesigned many of them, but here are links to some of the orginal artists who created these wonderful wallpapers:

- EVA: [wallpaper](https://youtu.be/aFy2GrSOCD0?si=cOuglwx_EMJEPGwd), [font](https://www.1001fonts.com/electroharmonix-font.html)
  
## Supporting project

You can support me simply by dropping a **star** on **[github](https://github.com/Keyitdev/sddm-astronaut-theme)**, **[fork](https://github.com/the-og-ago/sddm-eva)** or giving a **subscription** on **[YouTube](http://www.youtube.com/channel/UCVoGVyAP2sHPQyegwBMJKyQ?sub_confirmation=1)**.

If you enjoyed it and would like to show your appreciation, you can make a **[donation](https://ko-fi.com/keyitdev)** using **[kofi](https://ko-fi.com/keyitdev)**.

[![Ko-fi](https://img.shields.io/badge/support_me_on_ko--fi-F16061?style=for-the-badge&logo=kofi&logoColor=f5f5f5)](https://ko-fi.com/keyitdev)

Distributed under the **[GPLv3+](https://www.gnu.org/licenses/gpl-3.0.html) License**.    
Copyright (C) 2022-2025 Keyitdev.
