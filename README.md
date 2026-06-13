# Flutter Setup Arch Linux

This flutter setup includes a pacman post transaction hook which clears flutter cache everytime the `flutter-bin` package is installed, upgraded or removed.

## Setup

On Arch-based distros:

```sh
$ sudo makepkg -si
```

On other distros:

```sh
$ sudo install flutter-cache-cleanup.hook /etc/pacman.d/hooks/zz-flutter-cache-cleanup.hook
$ sudo install -m755 flutter-cache-cleanup /usr/local/bin/flutter-cache-cleanup
```

