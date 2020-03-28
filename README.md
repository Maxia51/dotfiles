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

I decided to install "Font-Awesome" and "Yosemite San Francisco Font"
```shell 

sudo pacman -S ttf-font-awesome

```

The Yosemite fonts are available into this repo.
Just copy the .ttf into
