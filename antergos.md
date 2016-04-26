## Основное

## Оформление

### Темы

[Papirus](https://github.com/varlesh/papirus-suite)
```
# For KDE DE
yaourt -S papirus-icon-theme-kde papirus-gtk-theme papirus-look-and-feel plasma-theme-papirus
yaorut -S papirus-color-scheme papirus-qtcurve-theme papirus-aurorae-theme yakuake-skin-papirus
yaorut -S papirus-konsole-colorscheme papirus-kmail-theme papirus-k3b-theme
# For GTK DE
yaourt -S papirus-icon-theme-gtk
# For all DE
yaourt -S libreoffice-style-papirus
yaourt -S vlc-skin-papirus
yaourt -S smplayer-theme-papirus
yaourt -S bomi-skin-papirus
# Wallpapers for KDE DE
yaourt -S papirus-wallpapers-git
```
[Arc Dark](https://github.com/varlesh/Arc-Dark-KDE)
```
yaourt -S arc-dark-suite-git
```
Fix color menubar on GTK
```
sudo bash /usr/share/plasma/desktoptheme/Arc-Dark/fix-menubar.sh
```
Or add bash alias fix-menubar:
```
echo 'alias fix-menubar="sudo bash /usr/share/plasma/desktoptheme/Arc-Dark/fix-menubar.sh"' >> ~/.bashrc
```
Arc Dark Chromium theme

https://github.com/varlesh/Arc-Dark-KDE/raw/master/extra/chromium/Arc-Dark-KDE.crx


### Шрифты

**Noto Sans** (Сглаживание RGB, легкий хитинг).

Так же можно установить **MS-шрифты** из AUR:
```
yaourt -S ttf-ms-fonts
```

## Мультимедиа

KMix (для HDMI)
```
pacman -Ss kmix
```

## Интернет

## Разработка
