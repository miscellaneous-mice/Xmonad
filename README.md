# Xmonad

*This is a minimal install*

![Xmonad](https://github.com/miscellaneous-mice/Xmonad/assets/79500624/bb82dd74-69b3-40b7-9333-081a809edb2d)

### Installation
- First install Arch linux : https://github.com/miscellaneous-mice/Arch-install
- Go through the notes [Notes](https://github.com/miscellaneous-mice/Xmonad#note)
- Display drivers and Necessary packages
```
$ sudo pacman -S xorg xorg-server xorg-xinit xmonad xmonad-contrib alacritty ttf-fira-mono git picom
```
- Make the window manager config folder
```
mkdir ~/.xmonad
```
- Get the default configuration of xmonad
```
curl -o ~/.xmonad/xmonad.hs https://archives.haskell.org/code.haskell.org/xmonad/man/xmonad.hs
```
- Git clone my repo into home directory
```
$ git clone https://github.com/miscellaneous-mice/Xmonad.git
```
- Make a backup folder
```
$ mkdir ~/Backup
```
- Install the following dependencies below. Feel free to choose! [Dependencies](https://github.com/miscellaneous-mice/Xmonad#dependencies)

## Folder configuration

- These are the directories to be checked
```
~/.config/picom
~/.config/neofetch
~/.config/alacritty
~/.themes
~/.icons
~/.fonts
```
- If any of these folders are missing and make the missing directories
```
$ mkdir {missing-directory}
```
- Also make sure these specified directories are empty else move then into ```~/Backup/```
```
$ mv {directory}/* ~/Backup/
```
- Make the custom commands folder
```
$ mkdir ~/custom_commands/
```
- Copy the init files, but before that delete the existing .bashrc and .xinitrc files
```
$ mv ~/.bashrc ~/Backup/
$ cp ~/Xmonad/init_files/.xinitrc ~/
$ cp ~/Xmonad/init_files/.bashrc ~/
```
- Copy the figuration files as follows:
```
$ cp ~/Xmonad/xmonad/xmonad.hs ~/.xmonad/
$ cp ~/Xmonad/xmonad/.xmobarrc ~/
$ cp ~/Xmonad/alacritty/alacritty.yml ~/.config/alacritty/
$ cp ~/Xmonad/picom/picom.conf ~/.config/picom/
$ cp ~/Xmonad/neofetch/config.conf ~/.config/neofetch/
$ cp ~/Xmonad/custom_commands/.my_custom_commands.sh ~/custom_commands/
```
- Make these files executable
```
$ chmod +x ~/custom_commands/.my_custom_commands.sh
```
- Reboot ```sudo reboot```

## Extras
- Set the wallpaper
```
$ feh --bg-fill ~/Xmonad/wallpaper/blue.png
```
- Use lxappearance to apply the install the installed themes, icons and fonts.

### Dependencies
- thunar -> File manager
- feh -> Our wallpaper manager
- firefox -> Browser
- alsa-utils (alsamixer) -> Terminal audio control
- alacritty -> Terminal for our window manager
- lxappearance -> Used to set our themes, icons and fonts to our window manager and supported gtk-3 applications
- tty-clock -> Simplistic terminal clock
- dmenu -> Used to search applications
- xmobar -> Top bar to display information
- htop -> To display hardware resources being used
- nord theme (https://www.xfce-look.org/p/1267246/) -> Load into ~/.themes
- nord icons (https://www.xfce-look.org/p/1937741)  -> Load into ~/.icons
- Jetbrains nerd fonts (https://www.nerdfonts.com/font-downloads) -> Load into ~/.fonts
- Starship (https://starship.rs/) -> Alacritty terminal theme

## Note
- In ```~/.xinitrc``` file replace the display name and resolution with yours
```
xrandr --output {display-name} --mode resolution
```
- *You can find display this by just typing ```xrandr```*
- The shorcuts definition specified in comments may be wrong so kindly verify the code
- Run tty-clock in terminal by ```tty_clock_time```

## References
- https://travishorn.com/xmobar
- https://travishorn.com/the-xmonad-window-manager-on-arch-linux
