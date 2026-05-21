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

## VSCode
[Download .deb](https://code.visualstudio.com/Download)
```bash
sudo apt install ./code.deb
```
In preference settings :
Font : "FiraCode Nerd Font"
Font Ligature : True

View > Appearance > Move Primary Sidebar Right

## Docker & Compose
```bash
# Add Docker's official GPG key:
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/debian
Suites: $(. /etc/os-release && echo "$VERSION_CODENAME")
Components: stable
Architectures: $(dpkg --print-architecture)
Signed-By: /etc/apt/keyrings/docker.asc
EOF

sudo apt update
```
```bash
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
