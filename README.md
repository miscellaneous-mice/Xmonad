# Xmonad
*This is a minimal install*

### Installation
- First install Arch linux
- Xmonad installation
- ```sudo pacman -S xorg xorg-server xorg-xinit xf86-video-fbdev xmonad xmonad-contrib alacritty ttf-fira-mono git```
- ```git clone https://github.com/miscellaneous-mice/Xmonad.git```
- Install the given packages below. Feel free to choose.
- Folder configuration
```
- See which folder are missing before going to the next step
  ~/.xmonad
  ~/.config/picom
  ~/.config/neofetch
  ~/.themes
  ~/.icons
  ~/.fonts
- Else mkdir these folders

- Make the custom commands folder
    mkdir ~/custom_commands
```
- Copy the init files, but before that delete the existing .bashrc and .xinitrc files
```
- cp ~/Xmonad/init_files/.xinitrc ~/
- cp ~/Xmonad/init_files/.bashrc ~/ (Delete the old bashrc file)
```
- Copy the figuration files as follows:
```
- cp ~/Xmonad/xmonad/xmonad.hs ~/.xmonad/
- cp ~/Xmonad/xmonad/.xmobarrc ~/
- cp ~/Xmonad/alacritty/alacritty.yml ~/.config/alacritty/
- cp /etc/xdg/picom.conf ~/.config/picom/picom.conf
- cp ~/Xmonad/neofetch/config.conf ~/.config/neofetch
- cp ~/Xmonad/custom_commands/.my_custom_commands.sh ~/custom_commands/
```
- Reboot ```sudo reboot```
- Set the wallpaper
```feh --bg-fill /home/megame/Xmonad/wallpaper/blue.png```

### packages
- thunar -> File manager
- feh -> Our wallpaper manager
- firefox -> Browser
- alsamixer -> Terminal audio control
- alicritty -> Terminal for our window manager
- lxappearance -> Used to set our themes, icons and fonts to our window manager and supported gtk-3 applications
- tty-clock -> Simplistic terminal clock
- dmenu -> Used to search applications
- xmobar -> Top bar to display information
- nord theme ```(https://www.xfce-look.org/p/1267246/)``` -> Load into ~/.themes
- nord icons ```(https://www.xfce-look.org/p/1937741)```  -> Load into ~/.icons
- Jetbrains nerd fonts ```(https://www.nerdfonts.com/font-downloads)``` -> Load into ~/.fonts
- Starship ```(https://starship.rs/)``` -> Alacritty terminal theme

## Note
- In BSPWM/.xinitrc file replace the display name and resolution with yours
``` xrandr --output display-name --mode resolution```
- *You can find this by just typing ```xrandr```*

## References
- ```https://travishorn.com/xmobar```
- ```https://travishorn.com/the-xmonad-window-manager-on-arch-linux```
