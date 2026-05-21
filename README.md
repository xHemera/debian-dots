# Steps to fully setup a new Debian install (mostly for me to remember)

## Setup Sudo
```bash
su
sudo usermod -aG sudo hemera
systemctl reboot
```

## Setup Flatpak
```bash
sudo apt install flatpak
sudo apt install gnome-software-plugin-flatpak
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
systemctl reboot
```

## In Flatpak 
Install these apps :
- Vesktop
- Flatseal
- The Honkers Railway Launcher
- Extensions Manager
- Steam
- Zen Browser

## Settings
Appearance > Dark
Tweaks > Windows > Maximize / Minimize

## Extensions
### Dash to Panel
Hide Show Apps

### ArcMenu
To make it work :
```bash
sudo apt install libgnome-menu-3-0 gir1.2-gmenu-3.0
```
In settings :
Placement > Left
Layout > Modern > 11
Button > Icon > "Debian" > Size : 32

### Blur My Shell
Default settings

## Nerd Font
Install FiraCode
Copy all .ttf to .local/share/fonts
```bash
fc-cache -v -f
```

## VSCode
[Download .deb](https://code.visualstudio.com/Download)
```bash
sudo apt install ./code.deb
```
