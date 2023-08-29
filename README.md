### Thanks for Visiting! 
Welcome to my GitHub repository of personal dotfiles!

## Info
<table align="right">
   <tr>
      <th align="center">
         <sup><sub>:warning: WARNING :warning:</sub></sup>
      </th>
   </tr>
   <tr>
      <td align="center">
    
     This configuration was made for my Laptop,
     so some things might not work on your Laptop/PC
     as this was never intended to be a usable full fledged system
     
   </tr>
   </table>
   
|Distro|[Arch](https://archlinux.org/)|
|:---:|:---:|
|WM|[Hyprland](https://github.com/hyprwm/Hyprland)|
|Bar|[Waybar](https://github.com/Alexays/Waybar)|
|Menu|[Rofi for Wayland](https://github.com/lbonn/rofi)|
|Terminal|[Alacritty](https://github.com/alacritty/alacritty) / [Konsole](https://apps.kde.org/en/konsole)|
|File Manager|[Dolphin](https://archlinux.org/packages/extra/x86_64/dolphin/)|
|Shell|[Zsh](https://archlinux.org/packages/extra/x86_64/zsh/)|
|Aur Helper|[Paru](https://github.com/Morganamilo/paru)|
<br>

---
## Installation:
Below are the installation steps to install the dotfiles of my setup. Click on a step to Expand it.
<details>
<summary><b>1. Install Dependencies</b></summary> 
   
- Installation Hyprland Stuff:
```bash
paru -S --needed xdg-user-dirs hyprland-git hyprpicker-git waybar-hyprland-git \
networkmanager-dmenu-git rofi-lbonn-wayland alacritty dolphin firefox sddm-git \
qt5ct qt5-wayland qt6-wayland sway-bg xdg-desktop-portal-hyprland-git nwg-look \
dunst swaylock-effects-git pavucontrol blueberry redshift alsa-utils \
bluez bluez-utils bluez-libs bluez-tools grimblast-git wl-clipboard
```
- Install Terminal emulators
```bash
paru -S --needed konsole
```
or:
```bash
paru -S --needed alacritty
```
- Add your user to the Video Group and start the following services:
```bash
sudo usermod -aG video $USER
```
- Bluetooth:
```bash
sudo systemctl enable bluetooth
```

With that, we have all the dependencies. We can move to the next part.
</details>
<details>
<summary><b>2. Installing GTK/QT Theme</b></summary>
   
- To match with the current colorscheme, we are using the <a href="https://github.com/catppuccin">Catppuccin for GTK/QT/Cursor Theme</a>:
```bash
paru -S --needed catppuccin-gtk-theme-frappe catppuccin-cursors-frappe
```
- Clone them and install:
```bash
cd ~/Downloads
git clone https://github.com/catppuccin/qt5ct.git
cd qt5ct
cp -r themes/Catppuccin-Frappe.conf ~/.config/qt5ct/colors/
```
And that's it!
</details>
<details>
<summary><b>3. Installing Font/Emoji</b></summary>
   
Clone them and install: 
```bash
paru -S --needed ttf-jetbrains-mono-nerd noto-fonts noto-fonts-cjk noto-fonts-emoji
```
And that's it!
</details>
<details>
<summary><b>4. Installing Dotfiles</b></summary>
   
The step we all have been waiting for.
Clone them and install:
```bash
cd ~/Downloads
git clone https://github.com/VuDucNguyen9x/dotfiles.git
cd dotfiles
cp -r .config ~/
```
</details>

## Tips:

### 1. Get your directories.
If there are no default directories when you do `dir` or `ls`, you might just have to manually create them.
Just install `xdg-user-dirs` and run the command, then reboot.
```bash
xdg-user-dirs-update
```

#### Thanks to:
* [catppuccin](https://github.com/catppuccin)
* Creator Of [Archcraft OS](https://github.com/archcraft-os): [adi1090x](https://github.com/adi1090x)
* All the members of [r/unixporn](https://www.reddit.com/r/unixporn) community!
* And I forgot from where I took other code... :(

<p align="center"><b>That's it! Have a nice day!</b></p>
