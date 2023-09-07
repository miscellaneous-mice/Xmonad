# Xmonad

### Installation
- First install Arch linux
- Xmonad installation
- ```sudo pacman -S xorg xorg-server xorg-xinit xf86-video-fbdev xmonad xmonad-contrib alacritty ttf-fira-mono git```
- ```git clone https://github.com/miscellaneous-mice/Xmonad.git```
```
- cp ~/Xmonad/init_files/.xinitrc ~/
- cp ~/Xmonad/init_files/.bashrc ~/bashrc (Delete the old bashrc file)
- cp ~/Xmonad/xmonad/xmonad.hs ~/.xmonad/
- mkdir -p ~/.config/picom
- cp /etc/xdg/picom.conf ~/.config/picom/picom.conf
```
- Xmobar installation
```
- sudo pacman -S xmobar
- cp ~/Xmonad/xmonad/.xmobarrc ~/
```

### packages
- thunar
- feh
- firefox
- alsamixer
- alicritty
- lxappearance
- tty-clock (```git clone https://aur.archlinux.org/tty-clock.git```)
- dmenu
- xmobar
- nord theme ```(https://www.xfce-look.org/p/1267246/)``` -> Load into ~/.themes
- nord icons ```(https://www.xfce-look.org/p/1937741)```  -> Load into ~/.icons
- Jetbrains nerd fonts ```(https://www.nerdfonts.com/font-downloads)``` -> Load into ~/.fonts
- Starship ```(https://starship.rs/)```

## References
- ```https://travishorn.com/xmobar```
- ```https://travishorn.com/the-xmonad-window-manager-on-arch-linux```
