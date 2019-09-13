# Cosmos
A clean and lightweight space theme with minimal transparency for i3-gaps

<b>Overview:</b>
* OS: [Arch](https://www.archlinux.org/)
* WM: [i3-gaps](https://github.com/Airblader/i3)
* Bar: [py3status](https://github.com/ultrabug/py3status)
* Compositor: [Compton](https://github.com/chjj/compton)
* Terminal: [Termite](https://github.com/thestinger/termite)
* Menu: [Rofi](https://github.com/davatorium/rofi)
* Wallpaper: [Here](/wallpaper.jpg)

Apps running in screenshot: [Vim](https://github.com/vim/vim) (with [Powerline](https://github.com/powerline/powerline)), [Ranger](https://github.com/ranger/ranger), and [gotop](https://github.com/cjbassi/gotop).
<br>

<b>Features:</b>
* System Menu (Shutdown, Suspend, etc.): `$mod+e`
* Display Menu (Dock, HDMI, Mirror): `$mod+x`
* Screenshot (via Scrot): `$mod+p`
* Toggle Window Floating: `$mod+w`
* Seamlessly Switch Workspaces: `Mod1+tab`
* Exit Active Window: `Control+q`
* Rofi Menu: `$mod+d`<br>
<i>Simple drop-down menu with minimal transparency.  Place `custom.rasi` in `/usr/share/rofi/themes/`. Enable with `rofi-theme-selector`.</i>

User can modify these features and more in the i3 `.config`.

---

<b>Dependencies:</b><br>
<i>i3-gaps, i3status, py3status, i3lock-fancy-rapid, rofi, compton, lightdm, noto sans fonts, awesome fonts, ttf-monaco, termite, dunst, nitrogen, lxappearance, acpid, ntfs-3g, udisks2, udiskie, mesa (Intel GFX), lib32-mesa (Intel GFX), vulkan-intel (Intel GFX), powerline, alsa-utils, pulseaudio, pavucontrol, light (xbacklight alternative for laptops)</i>

<b>Optional:</b><br>
<i>yay, neofetech, network manager, network-manager-applet, bluez, bluez-utils, blueman, noto fonts extra, noto fonts cjk, noto fonts emoji, fcitx, fcitx-configtool, fcitx-mozc, fcitx-im, fcitx-skin-material, baobab, pcmanfm, cmus, cava, neofetch, gtk-engines, gtk-engine-murrine, materia-gtk-theme, flat-remix-gtk, htop, gotop, mons, indicator-sound-switcher, geany, scrot</i>

---

<b>IMPORTANT:</b><br>
It is assumed the user has lightdm autologin enabled.  i3lock-fancy-rapid will start upon boot.  To disable this feature, comment out `exec --no-startup-id sleep 1 && i3lock-fancy-rapid 5 3` in the i3 `.config` file.  

A custom service (i3lock.service) was created as a sleep hook.  The user name <b>must be modified</b>.  Place in `/etc/systemd/system/` and enable using `systemctl enable i3lock.service`.

The custom `i3status.conf` needs to be placed in `/etc/` in order for py3status to work after it is installed.

A custom module (`playerctl.py`) for py3status was used.  Place in `~/.config/py3status/modules/`.

Notebook users can place `30-touchpad.conf` in `/etc/X11/xorg.conf.d/` for trackpad gestures.

---

<b>Suggestions:</b><br>
i3 needs to be installed with the options of i3-gaps, i3-status, and i3-lock.  A compositor isn't required but is strongly recommended, especially to achieve the look and feel of this theme and transparency effects.  To that end, [compton](https://github.com/chjj/compton) is the best compositor for i3.  Lightdm is assumed to be the default display manager for this setup.

All other dependencies listed above should also be installed, especially if you are using a laptop with integrated Intel graphics.  Optional applications are also encouraged for the complete experience.

Dotfiles should be added to their respective locations according to the framework of the distrobution.  This installation guide assumes the user is on Arch Linux so please refer to the [wiki page](https://wiki.archlinux.org/) for details concerning each application.

For more customizations, go [here](https://thomashunter.name/i3-configurator/) for i3 colors and [here](http://terminal.sexy/) for terminal colors.

---

<b>Disclaimer:</b><br>
<i>I am in no way, shape, or form, responsible for anything that YOU did wrong to your own system.  The user should assume the risks involved before these configurations are attempted.</i>

![GitHub Logo](/screenshot.png)
