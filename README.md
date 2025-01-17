# Hyprland and KDE config files from Jens
## Hyprland
![Screenshot](https://raw.githubusercontent.com/JensDeLeersnyderPXL/arch-dotfiles/main/screenshots/hyprland_screenshot.png)

## KDE 
![Screenshot](https://raw.githubusercontent.com/JensDeLeersnyderPXL/arch-dotfiles/main/screenshots/KDE_screenshot.png)

## Install
## Install Arch
Switch keyboard layout
```
loadkeys be-latin1
```
Connect to wifi
```
iwctl
device list
station wlan0 scan
station wlan0 get-networks
station wlan0 connect "Name of Network/WiFi"
```
Install OS
```
archinstall
```
### Yay

Run as user NOT ROOT!
```
git clone https://aur.archlinux.org/yay-bin
cd yay-bin
makepkg -si
```

### Packages
```
yay -S vim tldr nano micro brave-bin vscode json-c curl cmake python-pip libappindicator-gtk3 github-desktop-bin onlyoffice-bin envycontrol nvidia-settings signal-desktop nvidia ntfs-3g git rocketchat-desktop paru downgrade zfz packagekit-qt5 oh-my-zsh-git
```

## Configuration Sddm /etc/sddm.conf
```
Session=Hyprland.desktop
User=Jens
Numlock=true
```

## Install Caskaydiacode nerd font mono
```
yay -S nerd-fonts-meta
```
## install hyprland
```
yay -S hyperland-bin sddm-git waybar-hyprland
```
## Waybar Weather
### Install python module
```
pip install requests
```
## Install nvidia drivers
```
yay -S nvidia
```
# KDE-Plasma
## install KDE
```
yay -S plsama kde-network-meta kde-system-meta kde-utilities-meta plasma-wayland-session
```
- Global Theme used: [Utterly Sweet](https://store.kde.org/p/1906500)
- SDDM   Theme used: [Sweet](https://github.com/EliverLara/Sweet/tree/nova/kde/sddm)
- Package   Updates: [Command Output](https://store.kde.org/p/1166510/)

## KDE restore/backup tools
- [Transfuse](https://gitlab.com/cscs/transfuse)
### install [Konsave](https://github.com/Prayag2/konsave)
```
pip install konsave
```
### add alias to your shell
```
alias konsave="/home/${USER}/.local/bin/konsave"
```
### Backup
```
konsave --export-profile profile_name
```
### Restore
```
konsave --import-profile path/to/profile_name.knsv
```
## Sources used making these

- Official Hyprland Github <https://github.com/hyprwm/Hyprland>
- Linux Mobiles Hyprland dot files <https://github.com/linuxmobile/hyprland-dots>
- Christitus Start <https://github.com/ChrisTitusTech/hyprland-titus>
