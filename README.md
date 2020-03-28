# dotfiles

## Abstract 

This Project will keep a trace of what I have done for my Manjaro configuration, in order to be able to reproduce my configuration on any computer.

## Configutation

Window manager: I3-Gaps.
Compositing window manager: Picom.

## Installation process

I3 installation :
```shell

# Here i choose to select number 1 3 4 5
sudo pacman -S i3

```

Picom installation :
```shell

sudo pacman -S picom
# keeping the system configuration file consistency
cp /etc/xdg/picom.conf ~/.config/picom.conf 

```

I3 configuration :
Just copy the i3 config file.
