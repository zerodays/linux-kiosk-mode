# Linux Kiosk Mode
Kiosk mode configuration and instructions using Sway and Plymouth on top of Debian Linux. Also includes Grub and GDM theme.

Launches a sample Flutter application because we use Flutter for some of our projects. Can launch any binary.

### Why?
We need a kiosk mode desktop environment for a touch only interface.

Why **Debian**? - Stability, should work on most other distros too.

Why **Sway**? - Lightweight, configurable, and we have previous experience with it.

Why **Plymouth**? - Is there any better alternative? Take a look at our custom plymouth themes [here](https://github.com/zerodays/plymouth-boobies).

Why **Grub**? - Because Debian uses Grub by default. Once they switch to systemd boot we will too.

Why **GDM**? - Easy configuration with support for smooth transition from plymouth to display manager and then sway.

Why **Flutter**? - Best frontend framework at the time. We hope it gets better support for linux.

### Quick tips
1. Shortcuts:
    - `SUPER`+`RETURN` - Start terminal.
    - `SUPER`+`Q` - Kill current application.
    - `SUPER`+`F` - Toggle fullscreen.
    - `SUPER`+`SHIFT`+`C` - Reload sway configuration.
    - `SUPER`+`SHIFT`+`E` - Exit sway.
2. Wallpaper:
    - Replace `~/wallpaper.jpg` to change wallpaper. Sway also supports other image formats - change wallpaper location in `~/.config/sway/config`.
3. Change/disable startup application:
    - Edit the last line of `~/.config/sway/config`.

# Installation instructions
1. Install Debian (11 or higher for easier sway installation) without any addons or desktop managers.
2. Build your [flutter app](flutter/flutter.md) (also works with any other binary). Copy it to the home folder.
2. Install `sway` package. Debian 10 and lower requires [manual installation](https://github.com/swaywm/sway/wiki/Debian-10-(Buster)-Installation).
3. Install `gdm3` and reboot. When GDM loads, select sway as your window manager and log in.
4. Configure [sway](sway/sway.md).
5. Configure [GDM](gdm/gdm.md) auto login.
6. Install and configure [plymouth](plymouth/plymouth.md).
7. Hide [grub](grub/grub.md).
8. You might want to lock BIOS with password.

### TODO:
- Configure sway touch input.
- Avoid installing entire gnome group with gdm3.