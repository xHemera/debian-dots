# Steps to fully setup a new Debian install (mostly for me to remember)

## 0. Setup Sudo
```bash
su
sudo usermod -aG sudo hemera
```

## 1. Setup Flatpak
```bash
sudo apt install flatpak
sudo apt install gnome-software-plugin-flatpak
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
systemctl reboot
```
