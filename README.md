# dotfiles

## Abstract 

This Project will keep a trace of what I have done for my Manjaro configuration, in order to be able to reproduce my configuration on any computer.

## Configutation

Window manager: I3-Gaps.
Compositing window manager: Picom.
File Manager: Nemo.
Main Theme: Nord.
Terminal: xrvt-unicode.
Shell: zsh | prezto.

## Installation process

### I3 

I3 installation :
```shell

# Here choose to select number 1 3 4 5
sudo pacman -S i3

```

### Picom

Picom installation :
```shell

sudo pacman -S picom

```

### Polybar

```shell

git clone https://github.com/polybar/polybar.git
cd polybar
makepkg -si

```

### Rxvt


```shell

sudo pacman -S rxvt-unicode

```

### Zsh | Prezto

```shell

# Zsh
sudo pacman -S zsh

# Prezto
git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"

setopt EXTENDED_GLOB
for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
  ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
done

```


### Docker

```shell

# Docker
sudo pacman -S docker
sudo pacman -S docker-compose

# Completion
curl -fLo ~/.zprezto/modules/completion/external/src/_docker https://raw.githubusercontent.com/docker/cli/master/contrib/completion/zsh/_docker
curl -fLo ~/.zprezto/modules/completion/external/src/_docker-compose https://raw.githubusercontent.com/docker/compose/master/contrib/completion/zsh/_docker-compose
exec $SHELL -l
compinit -i -c

```

### Fonts

Fonts are in `.fonts`

Fonts used: 
 - Font-Awesome `sudo pacman -S ttf-font-awesome`
 - [Yosemite San Francisco Font](https://github.com/supermarin/YosemiteSanFranciscoFont)

Don't forget to change the fonts in `~/.gtkrc-2.0` and `~/.config/gtk-3.0/settings.ini`

To render the fonts in a better way :
```shell
sudo pacman -S freetype2
sudo cp /etc/fonts/conf.avail/10-hinting-full.conf /etc/fonts/conf.d
sudo cp /etc/fonts/conf.avail/10-sub-pixel-rgb.conf /etc/fonts/conf.d
sudo cp /etc/fonts/conf.avail/11-lcdfilter-default.conf /etc/fonts/conf.d
```

### Applications

Here is global list of application to install :
- i3
- picom
- polybar
- lxapparence
- rxvt-unicode
- zsh | prezto
- docker
- docker-compose
- VS Code
- Discord Canary
- Spotify
- GitKraken
- Intellij Idea
- PHP Storm