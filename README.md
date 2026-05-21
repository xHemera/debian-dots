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

## Settings
Appearance > Dark
Tweaks > Windows > Maximize / Minimize

## Extensions
### Dash to Panel
Hide Show Apps

### ArcMenu

### Blur My Shell
Default settings
