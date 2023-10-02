# Xmonad

*This is a minimal install*

![Xmonad](https://github.com/miscellaneous-mice/Xmonad/assets/79500624/bb82dd74-69b3-40b7-9333-081a809edb2d)

### Installation
- First install Arch linux : https://github.com/miscellaneous-mice/Arch-install
- Go through the notes [Notes](https://github.com/miscellaneous-mice/Xmonad#note)
- Display drivers and Necessary packages
```
$ sudo pacman -S xorg xorg-server xorg-xinit xmonad xmonad-contrib alacritty xterm ttf-fira-mono git picom
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
~/.config
~/.config/picom
~/.config/neofetch
~/.config/alacritty
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
- Copy the init files, but before that move the existing .bashrc and .xinitrc files into backup folder
```
$ mv ~/.bashrc ~/Backup/
$ cp ~/Xmonad/init_files/.xinitrc ~/
$ cp ~/Xmonad/init_files/.bashrc ~/
```
- Start the basic window manager (ignore all the errors in terminal)
```
$ startx
```
- These are the basic commands to navigate the window manager
```
alt + shift + Enter : open terminal
alt + p : search programs
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

## Setting themes, icons, fonts, Mouse cursors, wallpapers, etc.
- First download these files into the Downloads folder
  - Theme -> https://www.xfce-look.org/p/1267246/
  - Icons -> https://www.xfce-look.org/p/1937741
  - Fonts -> https://www.nerdfonts.com/font-downloads (Jetbrains nerd fonts)
- Make the appropriate directories so lxappearance can recognise them
```
$ cd ~/
$ mkdir .icons .themes .fonts
```
- Download the appropriate tools for unzipping files
```
$ sudo pacman -S unzip
```
- Extract the downloaded files into appropriate directories. First cd into the folder where you've downloaded
```
$ tar -xf Nordic-darker.tar.xz -C ~/.themes/
$ tar -xf Zafiro-Nord-Black-Blue.tar.xz -C ~/.icons/
$ unzip JetBrainsMono.zip
$ mv *.ttf ~/.fonts/
```
- Set the wallpaper
```
$ feh --bg-fill ~/Xmonad/wallpaper/blue.png
```
- Install tty-clock
```
$ git clone https://github.com/xorg62/tty-clock.git
$ cd tty-clock
$ sudo make install
```

### Dependencies
- thunar -> File manager
- feh -> Our wallpaper manager
- firefox -> Browser
- alsa-utils (alsamixer) -> Terminal audio control
- alacritty -> Terminal for our window manager
- lxappearance -> Used to set our themes, icons and fonts to our window manager and supported gtk-3 applications
- dmenu -> Used to search applications
- xmobar -> Top bar to display information
- htop -> To display hardware resources being used
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
