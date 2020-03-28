# dotfiles

## Abstract 

This Project will keep a trace of what I have done for my Manjaro configuration, in order to be able to reproduce my configuration on any computer.

## Configutation

Window manager: I3-Gaps.
Compositing window manager: Picom.

## Installation process

### I3 

I3 installation :
```shell

# Here i choose to select number 1 3 4 5
sudo pacman -S i3

```

Then just copy the I3 configuration file in ~/.config/i3

### Picom

Picom installation :
```shell

sudo pacman -S picom
# keeping the system configuration file consistency
cp /etc/xdg/picom.conf ~/.config/picom.conf 

```

### Fonts

Fonts used: 
 - Font-Awesome `sudo pacman -S ttf-font-awesome`
 - [Yosemite San Francisco Font](https://github.com/supermarin/YosemiteSanFranciscoFont)

Just copy the Yosemite `*.ttf` into `/usr/shared/fonts/TTF`
Don't forget to change the `~/.gtkrc-2.0` and `~/.config/gtk-3.0/settings.ini`

To render the fonts in a better way :
```shell
sudo pacman -S freetype2
sudo cp /etc/fonts/conf.avail/10-hinting-full.conf /etc/fonts/conf.d
sudo cp /etc/fonts/conf.avail/10-sub-pixel-rgb.conf /etc/fonts/conf.d
sudo cp /etc/fonts/conf.avail/11-lcdfilter-default.conf /etc/fonts/conf.d
```
