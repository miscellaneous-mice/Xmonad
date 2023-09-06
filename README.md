# Xmonad

### Installation
- First install Arch linux
- ```sudo pacman -S xorg xorg-server xorg-xinit xmonad xmonad-contrib alacritty ttf-fira-mono git```
- ```git clone https://github.com/miscellaneous-mice/Xmonad.git```
```
- cp ~/Xmonad/init_files/.xinitrc ~/
- cp ~/Xmonad/init_files/.bashrc ~/bashrc (Delete the old bashrc file)
- cp ~/Xmonad/xmonad/xmonad.hs ~/.xmonad/
- mkdir -p ~/.config/picom
- cp /etc/xdg/picom.conf ~/.config/picom/picom.conf
```
- ```https://travishorn.com/xmobar```
- graphics driver ```sudo pacman -S xf86-video-fbdev``` -> [Enable 3D-acceleration]

### packages
- thunar
- feh
- firefox
- alsamixer
- copyq
- alicritty
- lxappearance
- tty-clock
- dmenu
- xmobar
- nord theme ```(https://www.xfce-look.org/p/1267246/)``` -> Load into ~/.themes
- nord icons ```(https://www.xfce-look.org/p/1937741)```  -> Load into ~/.icons
- Jetbrains nerd fonts ```(https://www.nerdfonts.com/font-downloads)``` -> Load into ~/.fonts
- Starship ```(https://starship.rs/)```

### Important Commands
- In ~/.xinitrc file at the top of the file
```xrandr --output Virtual-1 --mode 1920x1090```

